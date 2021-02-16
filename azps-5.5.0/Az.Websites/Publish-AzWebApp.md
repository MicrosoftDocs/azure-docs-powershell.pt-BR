---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118498"
---
# <span data-ttu-id="b1572-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b1572-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="b1572-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1572-102">SYNOPSIS</span></span>
<span data-ttu-id="b1572-103">Implanta um Azure Web App a partir de um arquivo ZIP, JAR ou WAR usando zipdeploy.</span><span class="sxs-lookup"><span data-stu-id="b1572-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="b1572-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1572-104">SYNTAX</span></span>

### <span data-ttu-id="b1572-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b1572-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1572-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b1572-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="b1572-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1572-107">DESCRIPTION</span></span>
<span data-ttu-id="b1572-108">O cmdlet **Publish-AzWebApp** carrega conteúdo em um Azure Web App existente.</span><span class="sxs-lookup"><span data-stu-id="b1572-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="b1572-109">O conteúdo deve ser empacotado em um arquivo ZIP se estiver usando pilhas como .NET, Python ou Node, ou um arquivo WAR ou JAR se estiver usando Java.</span><span class="sxs-lookup"><span data-stu-id="b1572-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="b1572-110">O conteúdo deve ser pré-criado e pronto para ser executado sem etapas de com build adicionais durante a implantação.</span><span class="sxs-lookup"><span data-stu-id="b1572-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="b1572-111">Este cmdlet usa os recursos kudu zipdeploy e wardeploy para implantar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b1572-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="b1572-112">Consulte o wiki de Kudu para obter detalhes sobre como o zipdeploy e a wardeploy funcionam e como empacotar corretamente um aplicativo Web para implantação.</span><span class="sxs-lookup"><span data-stu-id="b1572-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="b1572-113"> https://aka.ms/kuduzipdeploy e contenham detalhes úteis sobre https://aka.ms/kuduwardeploy zipdeploy e wardeploy.</span><span class="sxs-lookup"><span data-stu-id="b1572-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="b1572-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b1572-114">EXAMPLES</span></span>

### <span data-ttu-id="b1572-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1572-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="b1572-116">Carrega o conteúdo do app.zip para o aplicativo Web chamado MyApp pertencente ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b1572-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="b1572-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b1572-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="b1572-118">Carrega o conteúdo de javaproject.war para o slot de Preparação do aplicativo Web chamado ContosoApp pertencente ao grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="b1572-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="b1572-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b1572-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="b1572-120">Carrega o conteúdo do app.zip para o aplicativo Web chamado ContosoApp pertencente ao grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="b1572-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="b1572-121">O cmdlet será executado em um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b1572-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="b1572-122">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="b1572-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="b1572-123">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="b1572-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="b1572-124">Carrega o conteúdo de java_app.jar para o aplicativo Web chamado ContosoApp pertencente ao grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="b1572-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="b1572-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1572-125">PARAMETERS</span></span>

### <span data-ttu-id="b1572-126">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="b1572-126">-ArchivePath</span></span>
<span data-ttu-id="b1572-127">O caminho do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="b1572-127">The path of the archive file.</span></span> <span data-ttu-id="b1572-128">ZIP, WAR e JAR são suportados.</span><span class="sxs-lookup"><span data-stu-id="b1572-128">ZIP, WAR, and JAR are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1572-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1572-129">-AsJob</span></span>
<span data-ttu-id="b1572-130">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b1572-130">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1572-131">-Forçar</span><span class="sxs-lookup"><span data-stu-id="b1572-131">-Force</span></span>
<span data-ttu-id="b1572-132">Opção Remover Com Força</span><span class="sxs-lookup"><span data-stu-id="b1572-132">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1572-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1572-133">-DefaultProfile</span></span>
<span data-ttu-id="b1572-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1572-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1572-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1572-135">-Name</span></span>
<span data-ttu-id="b1572-136">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="b1572-136">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1572-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1572-137">-ResourceGroupName</span></span>
<span data-ttu-id="b1572-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1572-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1572-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="b1572-139">-Slot</span></span>
<span data-ttu-id="b1572-140">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="b1572-140">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1572-141">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b1572-141">-WebApp</span></span>
<span data-ttu-id="b1572-142">O objeto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="b1572-142">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1572-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1572-143">CommonParameters</span></span>
<span data-ttu-id="b1572-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1572-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1572-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1572-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1572-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="b1572-146">INPUTS</span></span>

### <span data-ttu-id="b1572-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b1572-147">System.String</span></span>

### <span data-ttu-id="b1572-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b1572-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b1572-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="b1572-149">OUTPUTS</span></span>

### <span data-ttu-id="b1572-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b1572-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b1572-151">Notas</span><span class="sxs-lookup"><span data-stu-id="b1572-151">NOTES</span></span>

## <span data-ttu-id="b1572-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1572-152">RELATED LINKS</span></span>
