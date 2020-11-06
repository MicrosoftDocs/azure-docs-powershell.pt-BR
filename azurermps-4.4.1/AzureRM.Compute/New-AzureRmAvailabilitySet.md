---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 2e3fc51410ff5a6fa9fca2aaeec0fe326012a8bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441396"
---
# <span data-ttu-id="ade90-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ade90-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="ade90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ade90-102">SYNOPSIS</span></span>
<span data-ttu-id="ade90-103">Cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="ade90-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ade90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ade90-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ade90-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ade90-105">DESCRIPTION</span></span>
<span data-ttu-id="ade90-106">O cmdlet **New-AzureRmAvailabilitySet** cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="ade90-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="ade90-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ade90-107">EXAMPLES</span></span>

### <span data-ttu-id="ade90-108">Exemplo 1: criar um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="ade90-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="ade90-109">Esse comando cria um conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ade90-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ade90-110">OS</span><span class="sxs-lookup"><span data-stu-id="ade90-110">PARAMETERS</span></span>

### <span data-ttu-id="ade90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade90-111">-DefaultProfile</span></span>
<span data-ttu-id="ade90-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ade90-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ade90-113">-Local</span><span class="sxs-lookup"><span data-stu-id="ade90-113">-Location</span></span>
<span data-ttu-id="ade90-114">Especifica o local para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="ade90-114">Specifies the location for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade90-115">Gerenciados por</span><span class="sxs-lookup"><span data-stu-id="ade90-115">-Managed</span></span>
<span data-ttu-id="ade90-116">Conjunto de disponibilidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="ade90-116">Managed Availability Set</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade90-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ade90-117">-Name</span></span>
<span data-ttu-id="ade90-118">Especifica um nome para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="ade90-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade90-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="ade90-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="ade90-120">Especifica a contagem de domínios com falha na plataforma.</span><span class="sxs-lookup"><span data-stu-id="ade90-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade90-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="ade90-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="ade90-122">Especifica a contagem de domínios de atualização de plataforma.</span><span class="sxs-lookup"><span data-stu-id="ade90-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade90-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade90-123">-ResourceGroupName</span></span>
<span data-ttu-id="ade90-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ade90-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade90-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="ade90-125">-Sku</span></span>
<span data-ttu-id="ade90-126">O nome do SKU</span><span class="sxs-lookup"><span data-stu-id="ade90-126">The Name of Sku</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade90-127">CommonParameters</span></span>
<span data-ttu-id="ade90-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade90-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ade90-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade90-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ade90-130">INPUTS</span></span>

## <span data-ttu-id="ade90-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ade90-131">OUTPUTS</span></span>

## <span data-ttu-id="ade90-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ade90-132">NOTES</span></span>

## <span data-ttu-id="ade90-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ade90-133">RELATED LINKS</span></span>

[<span data-ttu-id="ade90-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ade90-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="ade90-135">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ade90-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


