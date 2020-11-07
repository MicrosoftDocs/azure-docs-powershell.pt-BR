---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: 03e121493d8112116f5e8fc6ed492a54b67d47d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776981"
---
# <span data-ttu-id="acca8-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="acca8-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="acca8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="acca8-102">SYNOPSIS</span></span>
<span data-ttu-id="acca8-103">Cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="acca8-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="acca8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acca8-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acca8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="acca8-105">DESCRIPTION</span></span>
<span data-ttu-id="acca8-106">O cmdlet **New-AzAvailabilitySet** cria um conjunto de disponibilidade do Azure.</span><span class="sxs-lookup"><span data-stu-id="acca8-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="acca8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="acca8-107">EXAMPLES</span></span>

### <span data-ttu-id="acca8-108">Exemplo 1: criar um conjunto de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="acca8-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="acca8-109">Esse comando cria um conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="acca8-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="acca8-110">OS</span><span class="sxs-lookup"><span data-stu-id="acca8-110">PARAMETERS</span></span>

### <span data-ttu-id="acca8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="acca8-111">-AsJob</span></span>
<span data-ttu-id="acca8-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="acca8-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="acca8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acca8-113">-DefaultProfile</span></span>
<span data-ttu-id="acca8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="acca8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acca8-115">-Local</span><span class="sxs-lookup"><span data-stu-id="acca8-115">-Location</span></span>
<span data-ttu-id="acca8-116">Especifica o local para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="acca8-116">Specifies the location for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acca8-117">Gerenciados por</span><span class="sxs-lookup"><span data-stu-id="acca8-117">-Managed</span></span>
<span data-ttu-id="acca8-118">Conjunto de disponibilidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="acca8-118">Managed Availability Set</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acca8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="acca8-119">-Name</span></span>
<span data-ttu-id="acca8-120">Especifica um nome para o conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="acca8-120">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acca8-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="acca8-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="acca8-122">Especifica a contagem de domínios com falha na plataforma.</span><span class="sxs-lookup"><span data-stu-id="acca8-122">Specifies the platform fault domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acca8-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="acca8-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="acca8-124">Especifica a contagem de domínios de atualização de plataforma.</span><span class="sxs-lookup"><span data-stu-id="acca8-124">Specifies the platform update domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acca8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acca8-125">-ResourceGroupName</span></span>
<span data-ttu-id="acca8-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="acca8-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="acca8-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="acca8-127">-Sku</span></span>
<span data-ttu-id="acca8-128">O nome do SKU</span><span class="sxs-lookup"><span data-stu-id="acca8-128">The Name of Sku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acca8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acca8-129">CommonParameters</span></span>
<span data-ttu-id="acca8-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acca8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acca8-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acca8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acca8-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="acca8-132">INPUTS</span></span>

### <span data-ttu-id="acca8-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="acca8-133">None</span></span>
<span data-ttu-id="acca8-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="acca8-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="acca8-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="acca8-135">OUTPUTS</span></span>

### <span data-ttu-id="acca8-136">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="acca8-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="acca8-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="acca8-137">NOTES</span></span>

## <span data-ttu-id="acca8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acca8-138">RELATED LINKS</span></span>

[<span data-ttu-id="acca8-139">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="acca8-139">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="acca8-140">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="acca8-140">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


