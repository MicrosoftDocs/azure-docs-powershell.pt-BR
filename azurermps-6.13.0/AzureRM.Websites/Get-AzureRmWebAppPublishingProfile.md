---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a59d747dd7ba91d69d364770c91baf1a21ffedd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429272"
---
# <span data-ttu-id="1fad8-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1fad8-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="1fad8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fad8-102">SYNOPSIS</span></span>
<span data-ttu-id="1fad8-103">Obtém um perfil de publicação do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1fad8-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fad8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fad8-104">SYNTAX</span></span>

### <span data-ttu-id="1fad8-105">Eles</span><span class="sxs-lookup"><span data-stu-id="1fad8-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fad8-106">S2</span><span class="sxs-lookup"><span data-stu-id="1fad8-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fad8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1fad8-107">DESCRIPTION</span></span>
<span data-ttu-id="1fad8-108">O cmdlet **Get-AzureRmWebAppPublishingProfile** Obtém um perfil de publicação do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1fad8-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="1fad8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fad8-109">EXAMPLES</span></span>

### <span data-ttu-id="1fad8-110">1:</span><span class="sxs-lookup"><span data-stu-id="1fad8-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="1fad8-111">Este comando obtém o perfil de publicação no formato FTP para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus e o armazena no arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="1fad8-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="1fad8-112">OS</span><span class="sxs-lookup"><span data-stu-id="1fad8-112">PARAMETERS</span></span>

### <span data-ttu-id="1fad8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fad8-113">-DefaultProfile</span></span>
<span data-ttu-id="1fad8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1fad8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fad8-115">-Format</span><span class="sxs-lookup"><span data-stu-id="1fad8-115">-Format</span></span>
<span data-ttu-id="1fad8-116">Format</span><span class="sxs-lookup"><span data-stu-id="1fad8-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fad8-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="1fad8-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="1fad8-118">Inclua os pontos de extremidade de recuperação de desastre se verdadeiro</span><span class="sxs-lookup"><span data-stu-id="1fad8-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fad8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fad8-119">-Name</span></span>
<span data-ttu-id="1fad8-120">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="1fad8-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fad8-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="1fad8-121">-OutputFile</span></span>
<span data-ttu-id="1fad8-122">Arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="1fad8-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fad8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fad8-123">-ResourceGroupName</span></span>
<span data-ttu-id="1fad8-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1fad8-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fad8-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1fad8-125">-WebApp</span></span>
<span data-ttu-id="1fad8-126">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="1fad8-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fad8-127">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="1fad8-127">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="1fad8-128">Inclua os pontos de extremidade de recuperação de desastre se verdadeiro</span><span class="sxs-lookup"><span data-stu-id="1fad8-128">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fad8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fad8-129">CommonParameters</span></span>
<span data-ttu-id="1fad8-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fad8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fad8-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fad8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fad8-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1fad8-132">INPUTS</span></span>

### <span data-ttu-id="1fad8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1fad8-133">System.String</span></span>

### <span data-ttu-id="1fad8-134">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="1fad8-134">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="1fad8-135">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1fad8-135">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="1fad8-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1fad8-136">OUTPUTS</span></span>

### <span data-ttu-id="1fad8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1fad8-137">System.String</span></span>

## <span data-ttu-id="1fad8-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1fad8-138">NOTES</span></span>

## <span data-ttu-id="1fad8-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fad8-139">RELATED LINKS</span></span>

[<span data-ttu-id="1fad8-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1fad8-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="1fad8-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1fad8-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


