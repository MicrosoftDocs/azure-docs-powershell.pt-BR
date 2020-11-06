---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
ms.openlocfilehash: e17ac9d538424e3e7883060e6a3dcbec9c6a2c8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441464"
---
# <span data-ttu-id="94ac8-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="94ac8-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="94ac8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="94ac8-103">Obtém uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="94ac8-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94ac8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94ac8-104">SYNTAX</span></span>

### <span data-ttu-id="94ac8-105">NoExpandStandAloneNic (padrão)</span><span class="sxs-lookup"><span data-stu-id="94ac8-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94ac8-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="94ac8-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94ac8-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="94ac8-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94ac8-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="94ac8-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94ac8-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94ac8-109">DESCRIPTION</span></span>
<span data-ttu-id="94ac8-110">O cmdlet **Get-AzureRmNetworkInterface** Obtém uma interface de rede do Azure ou uma lista de interfaces de rede do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="94ac8-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="94ac8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94ac8-111">EXAMPLES</span></span>

### <span data-ttu-id="94ac8-112">Exemplo 1: obter todas as interfaces de rede</span><span class="sxs-lookup"><span data-stu-id="94ac8-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="94ac8-113">Este comando obtém todas as interfaces de rede para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="94ac8-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="94ac8-114">Exemplo 2: obter todas as interfaces de rede com um estado de provisionamento específico</span><span class="sxs-lookup"><span data-stu-id="94ac8-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="94ac8-115">Esse comando obtém todas as interfaces de rede no grupo de recursos chamado ResourceGroup1 que têm um estado de provisionamento de sucesso.</span><span class="sxs-lookup"><span data-stu-id="94ac8-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="94ac8-116">OS</span><span class="sxs-lookup"><span data-stu-id="94ac8-116">PARAMETERS</span></span>

### <span data-ttu-id="94ac8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ac8-117">-DefaultProfile</span></span>
<span data-ttu-id="94ac8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94ac8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94ac8-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="94ac8-119">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94ac8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="94ac8-120">-Name</span></span>
<span data-ttu-id="94ac8-121">Especifica o nome da interface de rede obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94ac8-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94ac8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94ac8-122">-ResourceGroupName</span></span>
<span data-ttu-id="94ac8-123">Especifica o nome do grupo de recursos a partir do qual esse cmdlet obtém interfaces de rede.</span><span class="sxs-lookup"><span data-stu-id="94ac8-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94ac8-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="94ac8-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="94ac8-125">Especifica o índice da máquina virtual do conjunto de escala da máquina virtual do qual este cmdlet obtém interfaces de rede.</span><span class="sxs-lookup"><span data-stu-id="94ac8-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94ac8-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="94ac8-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="94ac8-127">Especifica o nome do conjunto de escala da máquina virtual do qual este cmdlet obtém interfaces de rede.</span><span class="sxs-lookup"><span data-stu-id="94ac8-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94ac8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ac8-128">CommonParameters</span></span>
<span data-ttu-id="94ac8-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ac8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ac8-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94ac8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ac8-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94ac8-131">INPUTS</span></span>

### <span data-ttu-id="94ac8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="94ac8-132">System.String</span></span>

## <span data-ttu-id="94ac8-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94ac8-133">OUTPUTS</span></span>

### <span data-ttu-id="94ac8-134">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="94ac8-134">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="94ac8-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94ac8-135">NOTES</span></span>

## <span data-ttu-id="94ac8-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94ac8-136">RELATED LINKS</span></span>

[<span data-ttu-id="94ac8-137">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="94ac8-137">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="94ac8-138">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="94ac8-138">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="94ac8-139">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="94ac8-139">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


