---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 29ef83bf3ed0f423686e7ddf84bc82555bd09572
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426247"
---
# <span data-ttu-id="6b1dd-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="6b1dd-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="6b1dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="6b1dd-103">Obtém um perfil de publicação de slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6b1dd-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b1dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b1dd-104">SYNTAX</span></span>

### <span data-ttu-id="6b1dd-105">Eles</span><span class="sxs-lookup"><span data-stu-id="6b1dd-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b1dd-106">S2</span><span class="sxs-lookup"><span data-stu-id="6b1dd-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b1dd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b1dd-107">DESCRIPTION</span></span>
<span data-ttu-id="6b1dd-108">O cmdlet **Get-AzureRmWebAppSlotPublishingProfile** Obtém o perfil de publicação do aplicativo Web para o slot especificado.</span><span class="sxs-lookup"><span data-stu-id="6b1dd-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="6b1dd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b1dd-109">EXAMPLES</span></span>

### <span data-ttu-id="6b1dd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6b1dd-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="6b1dd-111">Esse comando obtém o perfil de publicação no formato FTP para o slot Slot001 pertinente ao ContosoWebApp do aplicativo Web associado ao grupo de recursos Default-Web-Oesteus e o armazena no arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="6b1dd-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="6b1dd-112">OS</span><span class="sxs-lookup"><span data-stu-id="6b1dd-112">PARAMETERS</span></span>

### <span data-ttu-id="6b1dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b1dd-113">-DefaultProfile</span></span>
<span data-ttu-id="6b1dd-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b1dd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b1dd-115">-Format</span><span class="sxs-lookup"><span data-stu-id="6b1dd-115">-Format</span></span>
<span data-ttu-id="6b1dd-116">Format</span><span class="sxs-lookup"><span data-stu-id="6b1dd-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b1dd-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="6b1dd-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="6b1dd-118">Inclua os pontos de extremidade de recuperação de desastre se verdadeiro</span><span class="sxs-lookup"><span data-stu-id="6b1dd-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="6b1dd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b1dd-119">-Name</span></span>
<span data-ttu-id="6b1dd-120">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="6b1dd-120">WebApp Name</span></span>

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

### <span data-ttu-id="6b1dd-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="6b1dd-121">-OutputFile</span></span>
<span data-ttu-id="6b1dd-122">Arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="6b1dd-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b1dd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b1dd-123">-ResourceGroupName</span></span>
<span data-ttu-id="6b1dd-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6b1dd-124">Resource Group Name</span></span>

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

### <span data-ttu-id="6b1dd-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="6b1dd-125">-Slot</span></span>
<span data-ttu-id="6b1dd-126">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="6b1dd-126">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b1dd-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6b1dd-127">-WebApp</span></span>
<span data-ttu-id="6b1dd-128">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="6b1dd-128">WebApp Object</span></span>

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

### <span data-ttu-id="6b1dd-129">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="6b1dd-129">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="6b1dd-130">Inclua os pontos de extremidade de recuperação de desastre se verdadeiro</span><span class="sxs-lookup"><span data-stu-id="6b1dd-130">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="6b1dd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b1dd-131">CommonParameters</span></span>
<span data-ttu-id="6b1dd-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b1dd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b1dd-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b1dd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b1dd-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b1dd-134">INPUTS</span></span>

### <span data-ttu-id="6b1dd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6b1dd-135">System.String</span></span>

### <span data-ttu-id="6b1dd-136">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="6b1dd-136">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="6b1dd-137">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b1dd-137">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="6b1dd-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b1dd-138">OUTPUTS</span></span>

### <span data-ttu-id="6b1dd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6b1dd-139">System.String</span></span>

## <span data-ttu-id="6b1dd-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b1dd-140">NOTES</span></span>

## <span data-ttu-id="6b1dd-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b1dd-141">RELATED LINKS</span></span>

[<span data-ttu-id="6b1dd-142">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="6b1dd-142">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="6b1dd-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6b1dd-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="6b1dd-144">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6b1dd-144">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
