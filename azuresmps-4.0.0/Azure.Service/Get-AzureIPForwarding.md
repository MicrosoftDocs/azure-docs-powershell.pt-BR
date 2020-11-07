---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BE661AC7-BA39-4D6A-8083-16CE9327DC08
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4c84155484435a9601af005393593040c9cfe4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946348"
---
# <span data-ttu-id="6585d-101">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="6585d-101">Get-AzureIPForwarding</span></span>

## <span data-ttu-id="6585d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6585d-102">SYNOPSIS</span></span>
<span data-ttu-id="6585d-103">Obtém o status do encaminhamento de IP.</span><span class="sxs-lookup"><span data-stu-id="6585d-103">Gets the status of IP forwarding.</span></span>

## <span data-ttu-id="6585d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6585d-104">SYNTAX</span></span>

### <span data-ttu-id="6585d-105">IaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="6585d-105">IaaSIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6585d-106">SlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="6585d-106">SlotIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6585d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6585d-107">DESCRIPTION</span></span>
<span data-ttu-id="6585d-108">O cmdlet **Get-AzureIPForwarding** Obtém o status do encaminhamento de IP.</span><span class="sxs-lookup"><span data-stu-id="6585d-108">The **Get-AzureIPForwarding** cmdlet gets the status of IP forwarding.</span></span>

## <span data-ttu-id="6585d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6585d-109">EXAMPLES</span></span>

### <span data-ttu-id="6585d-110">Exemplo 1: obter status de encaminhamento IP para uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="6585d-110">Example 1: Get IP forwarding status for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureIPForwarding
Disabled
```

<span data-ttu-id="6585d-111">Esse comando obtém uma máquina virtual chamada ContosoVM06 para o serviço chamado ContosoService e passa o objeto da máquina virtual para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="6585d-111">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="6585d-112">O cmdlet atual Obtém o status do encaminhamento de IP para essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6585d-112">The current cmdlet gets the status of IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="6585d-113">OS</span><span class="sxs-lookup"><span data-stu-id="6585d-113">PARAMETERS</span></span>

### <span data-ttu-id="6585d-114">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="6585d-114">-NetworkInterfaceName</span></span>
<span data-ttu-id="6585d-115">Especifica o nome do adaptador de rede para o qual esse cmdlet obtém o status de encaminhamento IP.</span><span class="sxs-lookup"><span data-stu-id="6585d-115">Specifies the name of the network adapter for which this cmdlet gets IP forwarding status.</span></span>

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

### <span data-ttu-id="6585d-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6585d-116">-Profile</span></span>
<span data-ttu-id="6585d-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6585d-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6585d-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6585d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6585d-119">-RoleName</span><span class="sxs-lookup"><span data-stu-id="6585d-119">-RoleName</span></span>
<span data-ttu-id="6585d-120">Especifica o nome de uma função de PaaS para a qual esse cmdlet obtém o status de encaminhamento IP.</span><span class="sxs-lookup"><span data-stu-id="6585d-120">Specifies the name of a PaaS role for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6585d-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6585d-121">-ServiceName</span></span>
<span data-ttu-id="6585d-122">Especifica o nome de um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="6585d-122">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="6585d-123">A função PaaS pertence ao serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="6585d-123">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="6585d-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="6585d-124">-Slot</span></span>
<span data-ttu-id="6585d-125">Especifica um slot de PaaS.</span><span class="sxs-lookup"><span data-stu-id="6585d-125">Specifies a PaaS slot.</span></span>
<span data-ttu-id="6585d-126">A função de PaaS para a qual esse cmdlet obtém o status de encaminhamento tem o slot especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6585d-126">The PaaS role for which this cmdlet gets forwarding status has the slot that this parameter specifies.</span></span>
<span data-ttu-id="6585d-127">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="6585d-127">Valid values are:</span></span> 

- <span data-ttu-id="6585d-128">Preparo</span><span class="sxs-lookup"><span data-stu-id="6585d-128">Production</span></span>
- <span data-ttu-id="6585d-129">Preparação</span><span class="sxs-lookup"><span data-stu-id="6585d-129">Staging</span></span> 

<span data-ttu-id="6585d-130">O valor padrão é produção.</span><span class="sxs-lookup"><span data-stu-id="6585d-130">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6585d-131">-VM</span><span class="sxs-lookup"><span data-stu-id="6585d-131">-VM</span></span>
<span data-ttu-id="6585d-132">Especifica o objeto da máquina virtual para o qual esse cmdlet obtém o status de encaminhamento IP.</span><span class="sxs-lookup"><span data-stu-id="6585d-132">Specifies the virtual machine object for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6585d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6585d-133">CommonParameters</span></span>
<span data-ttu-id="6585d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6585d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6585d-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6585d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6585d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6585d-136">INPUTS</span></span>

## <span data-ttu-id="6585d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6585d-137">OUTPUTS</span></span>

### <span data-ttu-id="6585d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6585d-138">System.String</span></span>

## <span data-ttu-id="6585d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6585d-139">NOTES</span></span>

## <span data-ttu-id="6585d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6585d-140">RELATED LINKS</span></span>

[<span data-ttu-id="6585d-141">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="6585d-141">Set-AzureIPForwarding</span></span>](./Set-AzureIPForwarding.md)


