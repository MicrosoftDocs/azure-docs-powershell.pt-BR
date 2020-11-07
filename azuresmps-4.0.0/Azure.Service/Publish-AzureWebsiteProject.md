---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945877"
---
# <span data-ttu-id="e48d0-101">Publish-AzureWebsiteProject</span><span class="sxs-lookup"><span data-stu-id="e48d0-101">Publish-AzureWebsiteProject</span></span>

## <span data-ttu-id="e48d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e48d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e48d0-103">Publicar um projeto da Web do Visual Studio em um site do Microsoft Azure usando o WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="e48d0-103">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>

## <span data-ttu-id="e48d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e48d0-104">SYNTAX</span></span>

### <span data-ttu-id="e48d0-105">ProjectFile</span><span class="sxs-lookup"><span data-stu-id="e48d0-105">ProjectFile</span></span>
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e48d0-106">Pacote</span><span class="sxs-lookup"><span data-stu-id="e48d0-106">Package</span></span>
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e48d0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e48d0-107">DESCRIPTION</span></span>
<span data-ttu-id="e48d0-108">Publicar um projeto da Web do Visual Studio em um site do Microsoft Azure usando o WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="e48d0-108">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>
<span data-ttu-id="e48d0-109">Pode pegar um pacote do WebDeploy e publicar diretamente ou fazer um projeto da Web do Visual Studio, compilar o projeto e publicar.</span><span class="sxs-lookup"><span data-stu-id="e48d0-109">It can either take a WebDeploy package and publish directly, or take a Visual Studio web project, build the project and publish.</span></span>
<span data-ttu-id="e48d0-110">Ele também pode substituir as cadeias de conexão no Web.config durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="e48d0-110">It can also replace the connection strings in the Web.config during publish.</span></span>

## <span data-ttu-id="e48d0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e48d0-111">EXAMPLES</span></span>

### <span data-ttu-id="e48d0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e48d0-112">Example 1</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

<span data-ttu-id="e48d0-113">Crie um projeto Web do Visual Studio com a configuração de "depuração" (significando uso Web.Debug.config) e publique em um site do Microsoft Azure usando o WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="e48d0-113">Build a Visual Studio web project with "Debug" configuration (meaning use Web.Debug.config) and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="e48d0-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e48d0-114">Example 2</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

<span data-ttu-id="e48d0-115">Publique um arquivo. zip do pacote do WebDeploy em um site do Microsoft Azure usando o WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="e48d0-115">Publish a WebDeploy Package .zip file to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="e48d0-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e48d0-116">Example 3</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

<span data-ttu-id="e48d0-117">Publicar uma pasta de pacote do WebDeploy em um site do Microsoft Azure usando o WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="e48d0-117">Publish a WebDeploy Package folder to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="e48d0-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="e48d0-118">Example 4</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

<span data-ttu-id="e48d0-119">Crie um projeto Web do Visual Studio, substitua a cadeia de conexão "DefaultConnection" no Web.config e publique em um site do Microsoft Azure usando o WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="e48d0-119">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="e48d0-120">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="e48d0-120">Example 5</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

<span data-ttu-id="e48d0-121">Crie um projeto Web do Visual Studio, substitua a cadeia de conexão "DefaultConnection" no Web.config e publique em um site do Microsoft Azure usando o WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="e48d0-121">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>
<span data-ttu-id="e48d0-122">Observe que-defaultconnect é um parâmetro dinâmico que é adicionado pela análise de Web.config.</span><span class="sxs-lookup"><span data-stu-id="e48d0-122">Notice that -DefaultConnection is a dynamic parameter which gets added by parsing Web.config.</span></span>

## <span data-ttu-id="e48d0-123">OS</span><span class="sxs-lookup"><span data-stu-id="e48d0-123">PARAMETERS</span></span>

### <span data-ttu-id="e48d0-124">-Configuração</span><span class="sxs-lookup"><span data-stu-id="e48d0-124">-Configuration</span></span>
<span data-ttu-id="e48d0-125">A configuração usada para construir o projeto de aplicativo Web do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e48d0-125">The configuration used to build the Visual Studio web application project.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e48d0-126">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e48d0-126">-ConnectionString</span></span>
<span data-ttu-id="e48d0-127">As cadeias de conexão a serem usadas para a implantação.</span><span class="sxs-lookup"><span data-stu-id="e48d0-127">The connection strings to use for the deployment.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e48d0-128">-DoNotDelete</span><span class="sxs-lookup"><span data-stu-id="e48d0-128">-DoNotDelete</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e48d0-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="e48d0-129">-Name</span></span>
<span data-ttu-id="e48d0-130">O nome do site da Web.</span><span class="sxs-lookup"><span data-stu-id="e48d0-130">The web site name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e48d0-131">-Package</span><span class="sxs-lookup"><span data-stu-id="e48d0-131">-Package</span></span>
<span data-ttu-id="e48d0-132">A pasta do pacote WebDeploy para o arquivo zip do projeto de aplicativo Web do Visual Studio a ser publicado.</span><span class="sxs-lookup"><span data-stu-id="e48d0-132">The WebDeploy package folder for zip file of the Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e48d0-133">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e48d0-133">-Profile</span></span>
<span data-ttu-id="e48d0-134">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e48d0-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e48d0-135">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e48d0-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e48d0-136">-ProjectFile</span><span class="sxs-lookup"><span data-stu-id="e48d0-136">-ProjectFile</span></span>
<span data-ttu-id="e48d0-137">O projeto de aplicativo Web do Visual Studio a ser publicado.</span><span class="sxs-lookup"><span data-stu-id="e48d0-137">The Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e48d0-138">-Parameters</span><span class="sxs-lookup"><span data-stu-id="e48d0-138">-SetParametersFile</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e48d0-139">-SkipAppData</span><span class="sxs-lookup"><span data-stu-id="e48d0-139">-SkipAppData</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e48d0-140">-Slot</span><span class="sxs-lookup"><span data-stu-id="e48d0-140">-Slot</span></span>
<span data-ttu-id="e48d0-141">O nome do slot do site da Web.</span><span class="sxs-lookup"><span data-stu-id="e48d0-141">The web site slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e48d0-142">-Tokens</span><span class="sxs-lookup"><span data-stu-id="e48d0-142">-Tokens</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e48d0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e48d0-143">CommonParameters</span></span>
<span data-ttu-id="e48d0-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e48d0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e48d0-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e48d0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e48d0-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e48d0-146">INPUTS</span></span>

## <span data-ttu-id="e48d0-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e48d0-147">OUTPUTS</span></span>

## <span data-ttu-id="e48d0-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e48d0-148">NOTES</span></span>

## <span data-ttu-id="e48d0-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e48d0-149">RELATED LINKS</span></span>

[<span data-ttu-id="e48d0-150">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e48d0-150">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="e48d0-151">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e48d0-151">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="e48d0-152">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e48d0-152">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="e48d0-153">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e48d0-153">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


