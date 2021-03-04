---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 726f991f5e51b6196b61a6e977ba1c5d4a1debf0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901383"
---
# <span data-ttu-id="eb2a4-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eb2a4-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="eb2a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb2a4-102">SYNOPSIS</span></span>
<span data-ttu-id="eb2a4-103">Implanta um Aplicativo Web do Azure a partir de um arquivo ZIP, JAR ou WAR usando zipdeploy.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="eb2a4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eb2a4-104">SYNTAX</span></span>

### <span data-ttu-id="eb2a4-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="eb2a4-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb2a4-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="eb2a4-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="eb2a4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eb2a4-107">DESCRIPTION</span></span>
<span data-ttu-id="eb2a4-108">O cmdlet **Publish-AzWebApp** carrega conteúdo em um Aplicativo Web do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="eb2a4-109">O conteúdo deve ser empacotado em um arquivo ZIP se estiver usando pilhas como .NET, Python ou Node ou um arquivo WAR ou JAR se estiver usando Java.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="eb2a4-110">O conteúdo deve ser pré-criado e pronto para ser executado sem etapas de com build adicionais durante a implantação.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="eb2a4-111">Este cmdlet usa os recursos zipdeploy e wardeploy kudu para implantar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="eb2a4-112">Consulte o wiki kudu para obter detalhes sobre como o zipdeploy e wardeploy funcionam e como empacotar corretamente um aplicativo Web para implantação.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="eb2a4-113"> https://aka.ms/kuduzipdeploy e https://aka.ms/kuduwardeploy contêm detalhes úteis sobre zipdeploy e wardeploy.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="eb2a4-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb2a4-114">EXAMPLES</span></span>

### <span data-ttu-id="eb2a4-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eb2a4-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="eb2a4-116">Carrega o conteúdo de app.zip para o aplicativo Web chamado MyApp pertencente ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="eb2a4-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="eb2a4-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="eb2a4-118">Carrega o conteúdo de javaproject.war no slot de Preparação do aplicativo Web chamado ContosoApp pertencente ao grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="eb2a4-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="eb2a4-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="eb2a4-120">Carrega o conteúdo de app.zip para o aplicativo Web chamado ContosoApp pertencente ao grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="eb2a4-121">O cmdlet será executado em um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="eb2a4-122">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="eb2a4-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="eb2a4-123">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="eb2a4-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="eb2a4-124">Carrega o conteúdo de java_app.jar para o aplicativo Web chamado ContosoApp pertencente ao grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="eb2a4-125">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="eb2a4-125">Example 6</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Timeout 300000 -Force
```

<span data-ttu-id="eb2a4-126">Carrega o conteúdo de java_app.jar para o aplicativo Web chamado ContosoApp pertencente ao grupo de recursos ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-126">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="eb2a4-127">O usuário pode set the timespan in Milliseconds to wait before the request times out.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-127">User can Sets the timespan in Milliseconds to wait before the request times out.</span></span>

## <span data-ttu-id="eb2a4-128">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eb2a4-128">PARAMETERS</span></span>

### <span data-ttu-id="eb2a4-129">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="eb2a4-129">-ArchivePath</span></span>
<span data-ttu-id="eb2a4-130">O caminho do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-130">The path of the archive file.</span></span> <span data-ttu-id="eb2a4-131">ZIP, WAR e JAR são suportados.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-131">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="eb2a4-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb2a4-132">-AsJob</span></span>
<span data-ttu-id="eb2a4-133">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="eb2a4-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb2a4-134">-Force</span><span class="sxs-lookup"><span data-stu-id="eb2a4-134">-Force</span></span>
<span data-ttu-id="eb2a4-135">Opção Remover com força</span><span class="sxs-lookup"><span data-stu-id="eb2a4-135">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="eb2a4-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb2a4-136">-DefaultProfile</span></span>
<span data-ttu-id="eb2a4-137">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb2a4-138">-Name</span><span class="sxs-lookup"><span data-stu-id="eb2a4-138">-Name</span></span>
<span data-ttu-id="eb2a4-139">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-139">The name of the web app.</span></span>

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

### <span data-ttu-id="eb2a4-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb2a4-140">-ResourceGroupName</span></span>
<span data-ttu-id="eb2a4-141">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="eb2a4-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="eb2a4-142">-Slot</span></span>
<span data-ttu-id="eb2a4-143">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-143">The name of the web app slot.</span></span>

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

### <span data-ttu-id="eb2a4-144">-Timeout</span><span class="sxs-lookup"><span data-stu-id="eb2a4-144">-Timeout</span></span>
<span data-ttu-id="eb2a4-145">Define o tempo de tempo em Milissegundos para aguardar antes do tempo de solicitação.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-145">Sets the timespan in Milliseconds to wait before the request times out.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb2a4-146">-WebApp</span><span class="sxs-lookup"><span data-stu-id="eb2a4-146">-WebApp</span></span>
<span data-ttu-id="eb2a4-147">O objeto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="eb2a4-147">The web app object</span></span>

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

### <span data-ttu-id="eb2a4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb2a4-148">CommonParameters</span></span>
<span data-ttu-id="eb2a4-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb2a4-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb2a4-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb2a4-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb2a4-151">INPUTS</span></span>

### <span data-ttu-id="eb2a4-152">System.String</span><span class="sxs-lookup"><span data-stu-id="eb2a4-152">System.String</span></span>

### <span data-ttu-id="eb2a4-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="eb2a4-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="eb2a4-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eb2a4-154">OUTPUTS</span></span>

### <span data-ttu-id="eb2a4-155">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="eb2a4-155">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="eb2a4-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="eb2a4-156">NOTES</span></span>

## <span data-ttu-id="eb2a4-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb2a4-157">RELATED LINKS</span></span>
