---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 07ec4223414bbdbab8e3fa4d11641d040d918209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774286"
---
# <span data-ttu-id="29b5a-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="29b5a-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="29b5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="29b5a-103">Implanta um aplicativo Web do Azure de um arquivo ZIP, JAR ou WAR usando o zipdeploy.</span><span class="sxs-lookup"><span data-stu-id="29b5a-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="29b5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29b5a-104">SYNTAX</span></span>

### <span data-ttu-id="29b5a-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="29b5a-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29b5a-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="29b5a-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29b5a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29b5a-107">DESCRIPTION</span></span>
<span data-ttu-id="29b5a-108">O cmdlet **Publish-AzWebApp** carrega o conteúdo para um aplicativo Web do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="29b5a-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="29b5a-109">O conteúdo deve ser empacotado em um arquivo ZIP se estiver usando pilhas como .NET, Python ou nó ou um arquivo WAR ou JAR se estiver usando Java.</span><span class="sxs-lookup"><span data-stu-id="29b5a-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="29b5a-110">O conteúdo deve ser predefinido e pronto para ser executado sem nenhuma etapa adicional de compilação durante a implantação.</span><span class="sxs-lookup"><span data-stu-id="29b5a-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="29b5a-111">Este cmdlet usa os recursos kudu zipdeploy e wardeploy para implantar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="29b5a-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="29b5a-112">Consulte o wiki kudu para obter detalhes sobre como funciona o zipdeploy e o wardeploy e como empacotar corretamente um aplicativo Web para implantação.</span><span class="sxs-lookup"><span data-stu-id="29b5a-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="29b5a-113"> https://aka.ms/kuduzipdeploy e https://aka.ms/kuduwardeploy contém detalhes úteis sobre zipdeploy e wardeploy.</span><span class="sxs-lookup"><span data-stu-id="29b5a-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="29b5a-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29b5a-114">EXAMPLES</span></span>

### <span data-ttu-id="29b5a-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29b5a-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="29b5a-116">Carrega o conteúdo de app.zip para o aplicativo Web chamado MyApp pertencente ao grupo de recursos padrão-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="29b5a-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="29b5a-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="29b5a-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="29b5a-118">Carrega o conteúdo de javaproject. War para o slot de preparo do aplicativo Web chamado ContosoApp pertencente à ContosoRG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29b5a-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="29b5a-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="29b5a-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="29b5a-120">Carrega o conteúdo de app.zip para o aplicativo Web chamado ContosoApp pertencente ao grupo de ContosoRG de recursos.</span><span class="sxs-lookup"><span data-stu-id="29b5a-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="29b5a-121">O cmdlet será executado em um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="29b5a-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="29b5a-122">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="29b5a-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```

<span data-ttu-id="29b5a-123">Carrega o conteúdo de java_app. jar para o aplicativo Web nomeado ContosoApp pertencente à ContosoRG do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29b5a-123">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="29b5a-124">OS</span><span class="sxs-lookup"><span data-stu-id="29b5a-124">PARAMETERS</span></span>

### <span data-ttu-id="29b5a-125">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="29b5a-125">-ArchivePath</span></span>
<span data-ttu-id="29b5a-126">O caminho do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="29b5a-126">The path of the archive file.</span></span> <span data-ttu-id="29b5a-127">Há suporte para CEP, guerra e pote.</span><span class="sxs-lookup"><span data-stu-id="29b5a-127">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="29b5a-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29b5a-128">-AsJob</span></span>
<span data-ttu-id="29b5a-129">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="29b5a-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29b5a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b5a-130">-DefaultProfile</span></span>
<span data-ttu-id="29b5a-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29b5a-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29b5a-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="29b5a-132">-Name</span></span>
<span data-ttu-id="29b5a-133">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="29b5a-133">The name of the web app.</span></span>

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

### <span data-ttu-id="29b5a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29b5a-134">-ResourceGroupName</span></span>
<span data-ttu-id="29b5a-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29b5a-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="29b5a-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="29b5a-136">-Slot</span></span>
<span data-ttu-id="29b5a-137">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="29b5a-137">The name of the web app slot.</span></span>

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

### <span data-ttu-id="29b5a-138">-WebApp</span><span class="sxs-lookup"><span data-stu-id="29b5a-138">-WebApp</span></span>
<span data-ttu-id="29b5a-139">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="29b5a-139">The web app object</span></span>

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

### <span data-ttu-id="29b5a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b5a-140">CommonParameters</span></span>
<span data-ttu-id="29b5a-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29b5a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b5a-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29b5a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b5a-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29b5a-143">INPUTS</span></span>

### <span data-ttu-id="29b5a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="29b5a-144">System.String</span></span>

### <span data-ttu-id="29b5a-145">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="29b5a-145">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="29b5a-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29b5a-146">OUTPUTS</span></span>

### <span data-ttu-id="29b5a-147">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="29b5a-147">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="29b5a-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29b5a-148">NOTES</span></span>

## <span data-ttu-id="29b5a-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29b5a-149">RELATED LINKS</span></span>
