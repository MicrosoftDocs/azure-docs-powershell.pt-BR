---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA9686AF-2D03-43DB-A91B-50D06D674A3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8da83231a16f4c846f09d03374d6e35757e1ba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945956"
---
# <span data-ttu-id="e8bc1-101">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="e8bc1-101">Set-AzureIPForwarding</span></span>

## <span data-ttu-id="e8bc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="e8bc1-103">Habilita ou desabilita o encaminhamento de IP.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-103">Enables or disables IP forwarding.</span></span>

## <span data-ttu-id="e8bc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8bc1-104">SYNTAX</span></span>

### <span data-ttu-id="e8bc1-105">EnableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="e8bc1-105">EnableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e8bc1-106">DisableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="e8bc1-106">DisableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e8bc1-107">EnableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="e8bc1-107">EnableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e8bc1-108">DisableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="e8bc1-108">DisableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e8bc1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8bc1-109">DESCRIPTION</span></span>
<span data-ttu-id="e8bc1-110">O cmdlet **set-AzureIPForwarding** habilita ou desabilita o encaminhamento de IP para uma máquina virtual, para uma função de serviço de plataforma como serviço (PaaS) ou um adaptador de rede que pertence a uma máquina virtual ou função de PaaS.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-110">The **Set-AzureIPForwarding** cmdlet enables or disables IP forwarding for a virtual machine, for a platform as a service (PaaS) role, or a network adapter that belongs to a virtual machine or PaaS role.</span></span>

## <span data-ttu-id="e8bc1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8bc1-111">EXAMPLES</span></span>

### <span data-ttu-id="e8bc1-112">Exemplo 1: habilitar o encaminhamento de IP para uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e8bc1-112">Example 1: Enable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Enable
```

<span data-ttu-id="e8bc1-113">Esse comando obtém uma máquina virtual chamada ContosoVM06 para o serviço chamado ContosoService e passa o objeto da máquina virtual para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-113">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="e8bc1-114">O cmdlet atual habilita o encaminhamento de IP para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-114">The current cmdlet enables IP forwarding for that virtual machine.</span></span>

### <span data-ttu-id="e8bc1-115">Exemplo 2: desabilitar o encaminhamento de IP para uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e8bc1-115">Example 2: Disable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Disable
```

<span data-ttu-id="e8bc1-116">Esse comando obtém uma máquina virtual chamada ContosoVM06 para o serviço chamado ContosoService e passa o objeto da máquina virtual para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-116">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="e8bc1-117">O cmdlet atual desabilita o encaminhamento de IP para essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-117">The current cmdlet disables IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="e8bc1-118">OS</span><span class="sxs-lookup"><span data-stu-id="e8bc1-118">PARAMETERS</span></span>

### <span data-ttu-id="e8bc1-119">-Disable</span><span class="sxs-lookup"><span data-stu-id="e8bc1-119">-Disable</span></span>
<span data-ttu-id="e8bc1-120">Indica que esse cmdlet desabilita o encaminhamento de IP.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-120">Indicates that this cmdlet disables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableIaaSIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bc1-121">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="e8bc1-121">-Enable</span></span>
<span data-ttu-id="e8bc1-122">Indica que esse cmdlet habilita o encaminhamento de IP.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-122">Indicates that this cmdlet enables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableIaaSIPForwardingParamSet, EnableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bc1-123">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="e8bc1-123">-NetworkInterfaceName</span></span>
<span data-ttu-id="e8bc1-124">Especifica o nome do adaptador de rede no qual esse cmdlet define o encaminhamento de IP.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-124">Specifies the name of the network adapter on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bc1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8bc1-125">-PassThru</span></span>
<span data-ttu-id="e8bc1-126">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e8bc1-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e8bc1-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e8bc1-128">-Profile</span></span>
<span data-ttu-id="e8bc1-129">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e8bc1-130">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bc1-131">-RoleName</span><span class="sxs-lookup"><span data-stu-id="e8bc1-131">-RoleName</span></span>
<span data-ttu-id="e8bc1-132">Especifica o nome de uma função de PaaS na qual esse cmdlet define o encaminhamento de IP.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-132">Specifies the name of a PaaS role on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bc1-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e8bc1-133">-ServiceName</span></span>
<span data-ttu-id="e8bc1-134">Especifica o nome de um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-134">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="e8bc1-135">A função PaaS pertence ao serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-135">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bc1-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="e8bc1-136">-Slot</span></span>
<span data-ttu-id="e8bc1-137">Especifica um slot de PaaS.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-137">Specifies a PaaS slot.</span></span>
<span data-ttu-id="e8bc1-138">A função de PaaS para a qual esse cmdlet define Forwarding tem o slot que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-138">The PaaS role for which this cmdlet sets forwarding has the slot that this parameter specifies.</span></span>
<span data-ttu-id="e8bc1-139">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="e8bc1-139">Valid values are:</span></span>

- <span data-ttu-id="e8bc1-140">Preparo</span><span class="sxs-lookup"><span data-stu-id="e8bc1-140">Production</span></span>
- <span data-ttu-id="e8bc1-141">Preparação</span><span class="sxs-lookup"><span data-stu-id="e8bc1-141">Staging</span></span>

<span data-ttu-id="e8bc1-142">O valor padrão é produção.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-142">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bc1-143">-VM</span><span class="sxs-lookup"><span data-stu-id="e8bc1-143">-VM</span></span>
<span data-ttu-id="e8bc1-144">Especifica o objeto da máquina virtual em que este cmdlet define o encaminhamento de IP.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-144">Specifies the virtual machine object on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: EnableIaaSIPForwardingParamSet, DisableIaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bc1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8bc1-145">CommonParameters</span></span>
<span data-ttu-id="e8bc1-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8bc1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8bc1-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8bc1-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8bc1-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8bc1-148">INPUTS</span></span>

## <span data-ttu-id="e8bc1-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8bc1-149">OUTPUTS</span></span>

### <span data-ttu-id="e8bc1-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8bc1-150">System.Boolean</span></span>

## <span data-ttu-id="e8bc1-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8bc1-151">NOTES</span></span>

## <span data-ttu-id="e8bc1-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8bc1-152">RELATED LINKS</span></span>

[<span data-ttu-id="e8bc1-153">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="e8bc1-153">Get-AzureIPForwarding</span></span>](./Get-AzureIPForwarding.md)
