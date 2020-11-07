---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: ef00a9e425f67fbfc1ce47746503b574d483598f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785374"
---
# <span data-ttu-id="2c074-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2c074-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="2c074-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c074-102">SYNOPSIS</span></span>
<span data-ttu-id="2c074-103">Obtém conjuntos de disponibilidade do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c074-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c074-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c074-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c074-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c074-105">DESCRIPTION</span></span>
<span data-ttu-id="2c074-106">O cmdlet **Get-AzureRmAvailabilitySet** Obtém conjuntos de disponibilidade do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c074-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="2c074-107">Você pode especificar o nome de um conjunto de disponibilidade específico para obter.</span><span class="sxs-lookup"><span data-stu-id="2c074-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="2c074-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c074-108">EXAMPLES</span></span>

### <span data-ttu-id="2c074-109">Exemplo 1: obter um conjunto de disponibilidade específico</span><span class="sxs-lookup"><span data-stu-id="2c074-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="2c074-110">Esse comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2c074-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="2c074-111">Exemplo 2: obter todos os conjuntos de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="2c074-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="2c074-112">Esse comando obtém todos os conjuntos de disponibilidade no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2c074-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2c074-113">OS</span><span class="sxs-lookup"><span data-stu-id="2c074-113">PARAMETERS</span></span>

### <span data-ttu-id="2c074-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c074-114">-DefaultProfile</span></span>
<span data-ttu-id="2c074-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c074-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c074-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c074-116">-Name</span></span>
<span data-ttu-id="2c074-117">Especifica o nome de um conjunto de disponibilidade que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="2c074-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c074-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c074-118">-ResourceGroupName</span></span>
<span data-ttu-id="2c074-119">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c074-119">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c074-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c074-120">CommonParameters</span></span>
<span data-ttu-id="2c074-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c074-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c074-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c074-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c074-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c074-123">INPUTS</span></span>

### <span data-ttu-id="2c074-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2c074-124">None</span></span>
<span data-ttu-id="2c074-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2c074-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2c074-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c074-126">OUTPUTS</span></span>

### <span data-ttu-id="2c074-127">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2c074-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="2c074-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c074-128">NOTES</span></span>

## <span data-ttu-id="2c074-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c074-129">RELATED LINKS</span></span>

[<span data-ttu-id="2c074-130">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2c074-130">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="2c074-131">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2c074-131">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


