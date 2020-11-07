---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: df769ff4a6e4eb47bc47b881ac8c06de1fdb9e4c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775525"
---
# <span data-ttu-id="9e836-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9e836-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="9e836-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e836-102">SYNOPSIS</span></span>
<span data-ttu-id="9e836-103">Obtém uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="9e836-103">Gets a network interface.</span></span>

## <span data-ttu-id="9e836-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e836-104">SYNTAX</span></span>

### <span data-ttu-id="9e836-105">NoExpandStandAloneNic (padrão)</span><span class="sxs-lookup"><span data-stu-id="9e836-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e836-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="9e836-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e836-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="9e836-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e836-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="9e836-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e836-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e836-109">DESCRIPTION</span></span>
<span data-ttu-id="9e836-110">O cmdlet **Get-AzNetworkInterface** Obtém uma interface de rede do Azure ou uma lista de interfaces de rede do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9e836-110">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="9e836-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e836-111">EXAMPLES</span></span>

### <span data-ttu-id="9e836-112">Exemplo 1: obter todas as interfaces de rede</span><span class="sxs-lookup"><span data-stu-id="9e836-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzNetworkInterface
```

<span data-ttu-id="9e836-113">Este comando obtém todas as interfaces de rede para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9e836-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="9e836-114">Exemplo 2: obter todas as interfaces de rede com um estado de provisionamento específico</span><span class="sxs-lookup"><span data-stu-id="9e836-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="9e836-115">Esse comando obtém todas as interfaces de rede no grupo de recursos chamado ResourceGroup1 que têm um estado de provisionamento de sucesso.</span><span class="sxs-lookup"><span data-stu-id="9e836-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="9e836-116">OS</span><span class="sxs-lookup"><span data-stu-id="9e836-116">PARAMETERS</span></span>

### <span data-ttu-id="9e836-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e836-117">-DefaultProfile</span></span>
<span data-ttu-id="9e836-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e836-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e836-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="9e836-119">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e836-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e836-120">-Name</span></span>
<span data-ttu-id="9e836-121">Especifica o nome da interface de rede obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e836-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e836-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e836-122">-ResourceGroupName</span></span>
<span data-ttu-id="9e836-123">Especifica o nome do grupo de recursos a partir do qual esse cmdlet obtém interfaces de rede.</span><span class="sxs-lookup"><span data-stu-id="9e836-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e836-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="9e836-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="9e836-125">Especifica o índice da máquina virtual do conjunto de escala da máquina virtual do qual este cmdlet obtém interfaces de rede.</span><span class="sxs-lookup"><span data-stu-id="9e836-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e836-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9e836-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="9e836-127">Especifica o nome do conjunto de escala da máquina virtual do qual este cmdlet obtém interfaces de rede.</span><span class="sxs-lookup"><span data-stu-id="9e836-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e836-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e836-128">CommonParameters</span></span>
<span data-ttu-id="9e836-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e836-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e836-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e836-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e836-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e836-131">INPUTS</span></span>

## <span data-ttu-id="9e836-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e836-132">OUTPUTS</span></span>

### <span data-ttu-id="9e836-133">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9e836-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="9e836-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e836-134">NOTES</span></span>

## <span data-ttu-id="9e836-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e836-135">RELATED LINKS</span></span>

[<span data-ttu-id="9e836-136">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9e836-136">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="9e836-137">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9e836-137">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="9e836-138">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9e836-138">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


