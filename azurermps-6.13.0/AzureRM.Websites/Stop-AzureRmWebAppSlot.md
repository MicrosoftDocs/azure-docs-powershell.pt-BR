---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
ms.openlocfilehash: 2e6130b93a3c549ca84c2cb0a6a336f6afb177b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429983"
---
# <span data-ttu-id="bfb88-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bfb88-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="bfb88-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfb88-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb88-103">Interrompe um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bfb88-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfb88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfb88-104">SYNTAX</span></span>

### <span data-ttu-id="bfb88-105">Eles</span><span class="sxs-lookup"><span data-stu-id="bfb88-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfb88-106">S2</span><span class="sxs-lookup"><span data-stu-id="bfb88-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfb88-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfb88-107">DESCRIPTION</span></span>
<span data-ttu-id="bfb88-108">O cmdlet **Stop-AzureRmWebAppSlot** interrompe um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bfb88-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="bfb88-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfb88-109">EXAMPLES</span></span>

### <span data-ttu-id="bfb88-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bfb88-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="bfb88-111">Esse comando interrompe o slot Slot001 pertencente ao aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="bfb88-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="bfb88-112">OS</span><span class="sxs-lookup"><span data-stu-id="bfb88-112">PARAMETERS</span></span>

### <span data-ttu-id="bfb88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb88-113">-DefaultProfile</span></span>
<span data-ttu-id="bfb88-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb88-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfb88-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfb88-115">-Name</span></span>
<span data-ttu-id="bfb88-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="bfb88-116">WebApp Name</span></span>

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

### <span data-ttu-id="bfb88-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb88-117">-ResourceGroupName</span></span>
<span data-ttu-id="bfb88-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bfb88-118">Resource Group Name</span></span>

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

### <span data-ttu-id="bfb88-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="bfb88-119">-Slot</span></span>
<span data-ttu-id="bfb88-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="bfb88-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="bfb88-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bfb88-121">-WebApp</span></span>
<span data-ttu-id="bfb88-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="bfb88-122">WebApp Object</span></span>

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

### <span data-ttu-id="bfb88-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb88-123">CommonParameters</span></span>
<span data-ttu-id="bfb88-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb88-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb88-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb88-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb88-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfb88-126">INPUTS</span></span>

### <span data-ttu-id="bfb88-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bfb88-127">System.String</span></span>

### <span data-ttu-id="bfb88-128">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="bfb88-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="bfb88-129">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bfb88-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="bfb88-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfb88-130">OUTPUTS</span></span>

### <span data-ttu-id="bfb88-131">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="bfb88-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="bfb88-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfb88-132">NOTES</span></span>

## <span data-ttu-id="bfb88-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfb88-133">RELATED LINKS</span></span>
