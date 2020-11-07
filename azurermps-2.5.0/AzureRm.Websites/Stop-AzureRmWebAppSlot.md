---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: c59e40765fc5da07c5d079e3b5abd6224a8cbc5f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786032"
---
# <span data-ttu-id="fb48c-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fb48c-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="fb48c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb48c-102">SYNOPSIS</span></span>
<span data-ttu-id="fb48c-103">Interrompe um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fb48c-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb48c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb48c-104">SYNTAX</span></span>

### <span data-ttu-id="fb48c-105">Eles</span><span class="sxs-lookup"><span data-stu-id="fb48c-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb48c-106">S2</span><span class="sxs-lookup"><span data-stu-id="fb48c-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb48c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb48c-107">DESCRIPTION</span></span>
<span data-ttu-id="fb48c-108">O cmdlet **Stop-AzureRmWebAppSlot** interrompe um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fb48c-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="fb48c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb48c-109">EXAMPLES</span></span>

### <span data-ttu-id="fb48c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb48c-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="fb48c-111">Esse comando interrompe o slot Slot001 pertencente ao aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="fb48c-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="fb48c-112">OS</span><span class="sxs-lookup"><span data-stu-id="fb48c-112">PARAMETERS</span></span>

### <span data-ttu-id="fb48c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb48c-113">-DefaultProfile</span></span>
<span data-ttu-id="fb48c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb48c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb48c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb48c-115">-Name</span></span>
<span data-ttu-id="fb48c-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="fb48c-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb48c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb48c-117">-ResourceGroupName</span></span>
<span data-ttu-id="fb48c-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fb48c-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb48c-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="fb48c-119">-Slot</span></span>
<span data-ttu-id="fb48c-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="fb48c-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb48c-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fb48c-121">-WebApp</span></span>
<span data-ttu-id="fb48c-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="fb48c-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb48c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb48c-123">CommonParameters</span></span>
<span data-ttu-id="fb48c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb48c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb48c-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb48c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb48c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb48c-126">INPUTS</span></span>

### <span data-ttu-id="fb48c-127">Instalação</span><span class="sxs-lookup"><span data-stu-id="fb48c-127">Site</span></span>
<span data-ttu-id="fb48c-128">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="fb48c-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fb48c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb48c-129">OUTPUTS</span></span>

## <span data-ttu-id="fb48c-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb48c-130">NOTES</span></span>

## <span data-ttu-id="fb48c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb48c-131">RELATED LINKS</span></span>

