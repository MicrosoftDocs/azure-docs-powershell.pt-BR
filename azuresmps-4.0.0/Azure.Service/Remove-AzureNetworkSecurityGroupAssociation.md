---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E3E0237-8E2D-4B3A-AD0C-2121DDE1AAB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28259b97f382092f5e6293048c040688011cfe92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946152"
---
# <span data-ttu-id="106f8-101">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="106f8-101">Remove-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="106f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="106f8-102">SYNOPSIS</span></span>
<span data-ttu-id="106f8-103">Remove um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="106f8-103">Removes a network security group.</span></span>

## <span data-ttu-id="106f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="106f8-104">SYNTAX</span></span>

### <span data-ttu-id="106f8-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span><span class="sxs-lookup"><span data-stu-id="106f8-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="106f8-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span><span class="sxs-lookup"><span data-stu-id="106f8-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="106f8-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span><span class="sxs-lookup"><span data-stu-id="106f8-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> [-Slot <String>] -RoleName <String>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="106f8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="106f8-108">DESCRIPTION</span></span>
<span data-ttu-id="106f8-109">O cmdlet **Remove-AzureNetworkSecurityGroupAssociation** remove um grupo de segurança de rede de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="106f8-109">The **Remove-AzureNetworkSecurityGroupAssociation** cmdlet removes a network security group from a virtual machine.</span></span>

## <span data-ttu-id="106f8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="106f8-110">EXAMPLES</span></span>

### <span data-ttu-id="106f8-111">Exemplo 1: remover uma máquina virtual para um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="106f8-111">Example 1: Remove a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Remove-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="106f8-112">Esse comando obtém uma máquina virtual chamada ContosoVM06 para o serviço chamado ContosoService e passa o objeto da máquina virtual para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="106f8-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="106f8-113">O cmdlet atual remove o grupo de segurança de rede chamado ContosoNetworkSecurityGroup da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="106f8-113">The current cmdlet removes the network security group named ContosoNetworkSecurityGroup from that virtual machine.</span></span>

## <span data-ttu-id="106f8-114">OS</span><span class="sxs-lookup"><span data-stu-id="106f8-114">PARAMETERS</span></span>

### <span data-ttu-id="106f8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="106f8-115">-Force</span></span>
<span data-ttu-id="106f8-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="106f8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="106f8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="106f8-117">-Name</span></span>
<span data-ttu-id="106f8-118">Especifica o nome do grupo de segurança de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="106f8-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106f8-119">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="106f8-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="106f8-120">Especifica o nome do adaptador de rede do qual esse cmdlet Remove o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="106f8-120">Specifies the name of the network adapter from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="106f8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="106f8-121">-PassThru</span></span>
<span data-ttu-id="106f8-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="106f8-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="106f8-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="106f8-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="106f8-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="106f8-124">-Profile</span></span>
<span data-ttu-id="106f8-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="106f8-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="106f8-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="106f8-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="106f8-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="106f8-127">-RoleName</span></span>
<span data-ttu-id="106f8-128">Especifica o nome de uma função de PaaS da qual esse cmdlet Remove o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="106f8-128">Specifies the name of a PaaS role from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="106f8-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="106f8-129">-ServiceName</span></span>
<span data-ttu-id="106f8-130">Especifica o nome de um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="106f8-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="106f8-131">A função de PaaS da qual esse cmdlet Remove um grupo de segurança de rede pertence ao serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="106f8-131">The PaaS role from which this cmdlet removes a network security group belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="106f8-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="106f8-132">-Slot</span></span>
<span data-ttu-id="106f8-133">Especifica um slot de PaaS.</span><span class="sxs-lookup"><span data-stu-id="106f8-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="106f8-134">A função de PaaS da qual esse cmdlet Remove um grupo de segurança de rede tem o slot especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="106f8-134">The PaaS role from which this cmdlet removes a network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="106f8-135">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="106f8-135">Valid values are:</span></span>

- <span data-ttu-id="106f8-136">Preparo</span><span class="sxs-lookup"><span data-stu-id="106f8-136">Production</span></span>
- <span data-ttu-id="106f8-137">Preparação</span><span class="sxs-lookup"><span data-stu-id="106f8-137">Staging</span></span>

<span data-ttu-id="106f8-138">O valor padrão é produção.</span><span class="sxs-lookup"><span data-stu-id="106f8-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106f8-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="106f8-139">-SubnetName</span></span>
<span data-ttu-id="106f8-140">Especifica o nome de uma sub-rede da qual esse cmdlet Remove o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="106f8-140">Specifies the name of a subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106f8-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="106f8-141">-VirtualNetworkName</span></span>
<span data-ttu-id="106f8-142">Especifica o nome de uma rede virtual que contém a sub-rede da qual esse cmdlet Remove o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="106f8-142">Specifies the name of a virtual network that contains the subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106f8-143">-VM</span><span class="sxs-lookup"><span data-stu-id="106f8-143">-VM</span></span>
<span data-ttu-id="106f8-144">Especifica a máquina virtual para a qual esse cmdlet aplica o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="106f8-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="106f8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="106f8-145">CommonParameters</span></span>
<span data-ttu-id="106f8-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="106f8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="106f8-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="106f8-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="106f8-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="106f8-148">INPUTS</span></span>

## <span data-ttu-id="106f8-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="106f8-149">OUTPUTS</span></span>

### <span data-ttu-id="106f8-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="106f8-150">System.Boolean</span></span>

## <span data-ttu-id="106f8-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="106f8-151">NOTES</span></span>

## <span data-ttu-id="106f8-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="106f8-152">RELATED LINKS</span></span>

[<span data-ttu-id="106f8-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="106f8-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="106f8-154">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="106f8-154">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)
