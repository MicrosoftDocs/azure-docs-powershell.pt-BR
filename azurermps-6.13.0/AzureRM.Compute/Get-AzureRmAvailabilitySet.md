---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 685dafeb72693a617ca627aa1abcae19c5e24389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428574"
---
# <span data-ttu-id="ce783-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce783-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="ce783-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce783-102">SYNOPSIS</span></span>
<span data-ttu-id="ce783-103">Obtém conjuntos de disponibilidade do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ce783-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce783-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce783-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce783-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce783-105">DESCRIPTION</span></span>
<span data-ttu-id="ce783-106">O cmdlet **Get-AzureRmAvailabilitySet** Obtém conjuntos de disponibilidade do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ce783-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="ce783-107">Você pode especificar o nome de um conjunto de disponibilidade específico para obter.</span><span class="sxs-lookup"><span data-stu-id="ce783-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="ce783-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce783-108">EXAMPLES</span></span>

### <span data-ttu-id="ce783-109">Exemplo 1: obter um conjunto de disponibilidade específico</span><span class="sxs-lookup"><span data-stu-id="ce783-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="ce783-110">Esse comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ce783-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="ce783-111">Exemplo 2: obter todos os conjuntos de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="ce783-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="ce783-112">Esse comando obtém todos os conjuntos de disponibilidade no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ce783-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ce783-113">OS</span><span class="sxs-lookup"><span data-stu-id="ce783-113">PARAMETERS</span></span>

### <span data-ttu-id="ce783-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce783-114">-DefaultProfile</span></span>
<span data-ttu-id="ce783-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce783-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce783-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce783-116">-Name</span></span>
<span data-ttu-id="ce783-117">Especifica o nome de um conjunto de disponibilidade que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="ce783-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce783-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce783-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce783-119">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ce783-119">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce783-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce783-120">CommonParameters</span></span>
<span data-ttu-id="ce783-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce783-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce783-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce783-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce783-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce783-123">INPUTS</span></span>

### <span data-ttu-id="ce783-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ce783-124">System.String</span></span>

## <span data-ttu-id="ce783-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce783-125">OUTPUTS</span></span>

### <span data-ttu-id="ce783-126">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce783-126">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="ce783-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce783-127">NOTES</span></span>

## <span data-ttu-id="ce783-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce783-128">RELATED LINKS</span></span>

[<span data-ttu-id="ce783-129">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce783-129">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="ce783-130">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce783-130">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


