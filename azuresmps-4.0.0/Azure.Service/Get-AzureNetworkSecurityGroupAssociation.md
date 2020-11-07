---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 6AF7D392-8C8B-4695-95D0-E927093F654A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21eb1b7bcad200e67659f830bfb3bbef42fe0f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946582"
---
# <span data-ttu-id="3c82f-101">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="3c82f-101">Get-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="3c82f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c82f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c82f-103">Obtém um grupo de segurança de rede para uma máquina virtual, um adaptador de rede ou uma função de PaaS.</span><span class="sxs-lookup"><span data-stu-id="3c82f-103">Gets a network security group for a virtual machine, network adapter, or PaaS role.</span></span>

## <span data-ttu-id="3c82f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c82f-104">SYNTAX</span></span>

### <span data-ttu-id="3c82f-105">GetNetworkSecurityGroupAssociationForSubnet</span><span class="sxs-lookup"><span data-stu-id="3c82f-105">GetNetworkSecurityGroupAssociationForSubnet</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3c82f-106">GetNetworkSecurityGroupAssociationForIaaSRole</span><span class="sxs-lookup"><span data-stu-id="3c82f-106">GetNetworkSecurityGroupAssociationForIaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3c82f-107">GetNetworkSecurityGroupAssociationForPaaSRole</span><span class="sxs-lookup"><span data-stu-id="3c82f-107">GetNetworkSecurityGroupAssociationForPaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation [-Slot <String>] -RoleName <String> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3c82f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c82f-108">DESCRIPTION</span></span>
<span data-ttu-id="3c82f-109">O cmdlet **Get-AzureNetworkSecurityGroupAssociation** Obtém o grupo de segurança de rede para uma função de máquina virtual, adaptador de rede ou uma função de serviço de plataforma como serviço (PaaS).</span><span class="sxs-lookup"><span data-stu-id="3c82f-109">The **Get-AzureNetworkSecurityGroupAssociation** cmdlet gets the network security group for a virtual machine, network adapter, or platform as a service (PaaS) role.</span></span>

## <span data-ttu-id="3c82f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c82f-110">EXAMPLES</span></span>

### <span data-ttu-id="3c82f-111">Exemplo 1: obter o grupo de segurança de rede para uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="3c82f-111">Example 1: Get the network security group for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureNetworkSecurityGroupAssociation
```

<span data-ttu-id="3c82f-112">Esse comando obtém uma máquina virtual chamada ContosoVM06 para o serviço chamado ContosoService e passa o objeto da máquina virtual para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="3c82f-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="3c82f-113">O cmdlet atual Obtém o grupo de segurança de rede associado a essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3c82f-113">The current cmdlet gets the network security group associated to that virtual machine.</span></span>

## <span data-ttu-id="3c82f-114">OS</span><span class="sxs-lookup"><span data-stu-id="3c82f-114">PARAMETERS</span></span>

### <span data-ttu-id="3c82f-115">-Detalhado</span><span class="sxs-lookup"><span data-stu-id="3c82f-115">-Detailed</span></span>
<span data-ttu-id="3c82f-116">Indica que esse cmdlet retorna detalhes do grupo de segurança de rede associado à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3c82f-116">Indicates that this cmdlet returns details of the network security group that is associated to the virtual machine.</span></span>
<span data-ttu-id="3c82f-117">Esses detalhes incluem local e regras.</span><span class="sxs-lookup"><span data-stu-id="3c82f-117">These details include location and rules.</span></span>

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

### <span data-ttu-id="3c82f-118">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="3c82f-118">-NetworkInterfaceName</span></span>
<span data-ttu-id="3c82f-119">Especifica o nome do adaptador de rede para o qual esse cmdlet obtém o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="3c82f-119">Specifies the name of the network adapter for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c82f-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3c82f-120">-Profile</span></span>
<span data-ttu-id="3c82f-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="3c82f-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3c82f-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="3c82f-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c82f-123">-RoleName</span><span class="sxs-lookup"><span data-stu-id="3c82f-123">-RoleName</span></span>
<span data-ttu-id="3c82f-124">Especifica o nome de uma função de PaaS para a qual esse cmdlet obtém o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="3c82f-124">Specifies the name of a PaaS role for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c82f-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3c82f-125">-ServiceName</span></span>
<span data-ttu-id="3c82f-126">Especifica o nome de um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="3c82f-126">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="3c82f-127">A função PaaS pertence ao serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="3c82f-127">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c82f-128">-Slot</span><span class="sxs-lookup"><span data-stu-id="3c82f-128">-Slot</span></span>
<span data-ttu-id="3c82f-129">Especifica um slot de PaaS.</span><span class="sxs-lookup"><span data-stu-id="3c82f-129">Specifies a PaaS slot.</span></span>
<span data-ttu-id="3c82f-130">A função de PaaS para a qual esse cmdlet obtém o grupo de segurança de rede tem o slot especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3c82f-130">The PaaS role for which this cmdlet gets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="3c82f-131">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="3c82f-131">Valid values are:</span></span> 

- <span data-ttu-id="3c82f-132">Preparo</span><span class="sxs-lookup"><span data-stu-id="3c82f-132">Production</span></span>
- <span data-ttu-id="3c82f-133">Preparação</span><span class="sxs-lookup"><span data-stu-id="3c82f-133">Staging</span></span> 

<span data-ttu-id="3c82f-134">O valor padrão é produção.</span><span class="sxs-lookup"><span data-stu-id="3c82f-134">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c82f-135">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3c82f-135">-SubnetName</span></span>
<span data-ttu-id="3c82f-136">Especifica o nome de uma sub-rede para a qual esse cmdlet obtém o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="3c82f-136">Specifies the name of a subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c82f-137">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3c82f-137">-VirtualNetworkName</span></span>
<span data-ttu-id="3c82f-138">Especifica o nome de uma rede virtual que contém a sub-rede para a qual esse cmdlet obtém o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="3c82f-138">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c82f-139">-VM</span><span class="sxs-lookup"><span data-stu-id="3c82f-139">-VM</span></span>
<span data-ttu-id="3c82f-140">Especifica a máquina virtual para a qual esse cmdlet aplica o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="3c82f-140">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c82f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c82f-141">CommonParameters</span></span>
<span data-ttu-id="3c82f-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c82f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c82f-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c82f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c82f-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c82f-144">INPUTS</span></span>

## <span data-ttu-id="3c82f-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c82f-145">OUTPUTS</span></span>

### <span data-ttu-id="3c82f-146">Microsoft. WindowsAzure. Commands. immanagement. Network. NetworkSecurityGroup. Model. INetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c82f-146">Microsoft.WindowsAzure.Commands.ServiceManagement.Network.NetworkSecurityGroup.Model.INetworkSecurityGroup</span></span>

## <span data-ttu-id="3c82f-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c82f-147">NOTES</span></span>

## <span data-ttu-id="3c82f-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c82f-148">RELATED LINKS</span></span>

[<span data-ttu-id="3c82f-149">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="3c82f-149">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="3c82f-150">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="3c82f-150">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)


