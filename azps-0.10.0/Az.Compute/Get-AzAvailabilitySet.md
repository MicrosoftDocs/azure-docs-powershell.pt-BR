---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: ef42e8910b9ff6a71277c998825aa53cd3ad085e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777059"
---
# <span data-ttu-id="2f934-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2f934-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="2f934-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f934-102">SYNOPSIS</span></span>
<span data-ttu-id="2f934-103">Obtém conjuntos de disponibilidade do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2f934-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="2f934-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f934-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f934-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f934-105">DESCRIPTION</span></span>
<span data-ttu-id="2f934-106">O cmdlet **Get-AzAvailabilitySet** Obtém conjuntos de disponibilidade do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2f934-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="2f934-107">Você pode especificar o nome de um conjunto de disponibilidade específico para obter.</span><span class="sxs-lookup"><span data-stu-id="2f934-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="2f934-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f934-108">EXAMPLES</span></span>

### <span data-ttu-id="2f934-109">Exemplo 1: obter um conjunto de disponibilidade específico</span><span class="sxs-lookup"><span data-stu-id="2f934-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="2f934-110">Esse comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2f934-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="2f934-111">Exemplo 2: obter todos os conjuntos de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="2f934-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="2f934-112">Esse comando obtém todos os conjuntos de disponibilidade no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2f934-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2f934-113">OS</span><span class="sxs-lookup"><span data-stu-id="2f934-113">PARAMETERS</span></span>

### <span data-ttu-id="2f934-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f934-114">-DefaultProfile</span></span>
<span data-ttu-id="2f934-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f934-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f934-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f934-116">-Name</span></span>
<span data-ttu-id="2f934-117">Especifica o nome de um conjunto de disponibilidade que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="2f934-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2f934-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f934-118">-ResourceGroupName</span></span>
<span data-ttu-id="2f934-119">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2f934-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2f934-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f934-120">CommonParameters</span></span>
<span data-ttu-id="2f934-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f934-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f934-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f934-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f934-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f934-123">INPUTS</span></span>

### <span data-ttu-id="2f934-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2f934-124">None</span></span>
<span data-ttu-id="2f934-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2f934-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f934-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f934-126">OUTPUTS</span></span>

### <span data-ttu-id="2f934-127">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2f934-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="2f934-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f934-128">NOTES</span></span>

## <span data-ttu-id="2f934-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f934-129">RELATED LINKS</span></span>

[<span data-ttu-id="2f934-130">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2f934-130">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="2f934-131">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2f934-131">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


