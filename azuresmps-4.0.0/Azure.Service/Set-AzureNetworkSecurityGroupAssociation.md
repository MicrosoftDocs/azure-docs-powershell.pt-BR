---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 64639A35-0573-48C8-AB21-19FEB09537BA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b1b251a5fef3ad91f830e18714796421d2abca7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945758"
---
# <span data-ttu-id="1afda-101">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="1afda-101">Set-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="1afda-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1afda-102">SYNOPSIS</span></span>
<span data-ttu-id="1afda-103">Associa um grupo de segurança de rede a uma máquina virtual, função de PaaS ou adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="1afda-103">Associates a network security group to a virtual machine, PaaS role, or network adapter.</span></span>

## <span data-ttu-id="1afda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1afda-104">SYNTAX</span></span>

### <span data-ttu-id="1afda-105">AddNetworkSecurityGroupAssociationToSubnet</span><span class="sxs-lookup"><span data-stu-id="1afda-105">AddNetworkSecurityGroupAssociationToSubnet</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VirtualNetworkName <String>
 -SubnetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1afda-106">AddNetworkSecurityGroupAssociationToIaaSRole</span><span class="sxs-lookup"><span data-stu-id="1afda-106">AddNetworkSecurityGroupAssociationToIaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VM <PersistentVMRoleContext>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1afda-107">AddNetworkSecurityGroupAssociationToPaaSRole</span><span class="sxs-lookup"><span data-stu-id="1afda-107">AddNetworkSecurityGroupAssociationToPaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] [-Slot <String>]
 -RoleName <String> -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1afda-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1afda-108">DESCRIPTION</span></span>
<span data-ttu-id="1afda-109">O cmdlet **set-AzureNetworkSecurityGroupAssociation** associa um grupo de segurança de rede a um computador virtual, uma função de plataforma como serviço (PaaS) ou um adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="1afda-109">The **Set-AzureNetworkSecurityGroupAssociation** cmdlet associates a network security group to a virtual machine, platform as a service (PaaS) role, or network adapter.</span></span>

## <span data-ttu-id="1afda-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1afda-110">EXAMPLES</span></span>

### <span data-ttu-id="1afda-111">Exemplo 1: atribuir uma máquina virtual a um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="1afda-111">Example 1: Assign a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="1afda-112">Esse comando obtém uma máquina virtual chamada ContosoVM06 para o serviço chamado ContosoService e passa o objeto da máquina virtual para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="1afda-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="1afda-113">O cmdlet atual atribui o grupo de segurança de rede chamado ContosoNetworkSecurityGroup a essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1afda-113">The current cmdlet assigns the network security group named ContosoNetworkSecurityGroup to that virtual machine.</span></span>

## <span data-ttu-id="1afda-114">OS</span><span class="sxs-lookup"><span data-stu-id="1afda-114">PARAMETERS</span></span>

### <span data-ttu-id="1afda-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1afda-115">-Force</span></span>
<span data-ttu-id="1afda-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1afda-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1afda-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1afda-117">-Name</span></span>
<span data-ttu-id="1afda-118">Especifica o nome do grupo de segurança de rede que este cmdlet define.</span><span class="sxs-lookup"><span data-stu-id="1afda-118">Specifies the name of the network security group that this cmdlet sets.</span></span>

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

### <span data-ttu-id="1afda-119">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="1afda-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="1afda-120">Especifica o nome do adaptador de rede para o qual esse cmdlet aplica o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="1afda-120">Specifies the name of the network adapter to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1afda-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1afda-121">-PassThru</span></span>
<span data-ttu-id="1afda-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="1afda-122">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="1afda-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="1afda-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1afda-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1afda-124">-Profile</span></span>
<span data-ttu-id="1afda-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1afda-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1afda-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1afda-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1afda-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="1afda-127">-RoleName</span></span>
<span data-ttu-id="1afda-128">Especifica o nome de uma função de PaaS à qual esse cmdlet aplica o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="1afda-128">Specifies the name of a PaaS role to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1afda-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1afda-129">-ServiceName</span></span>
<span data-ttu-id="1afda-130">Especifica o nome de um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="1afda-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="1afda-131">A função PaaS pertence ao serviço que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1afda-131">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1afda-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="1afda-132">-Slot</span></span>
<span data-ttu-id="1afda-133">Especifica um slot de PaaS.</span><span class="sxs-lookup"><span data-stu-id="1afda-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="1afda-134">A função de PaaS para a qual esse cmdlet define o grupo de segurança de rede tem o slot especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1afda-134">The PaaS role for which this cmdlet sets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="1afda-135">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="1afda-135">Valid values are:</span></span> 

- <span data-ttu-id="1afda-136">Preparo</span><span class="sxs-lookup"><span data-stu-id="1afda-136">Production</span></span>
- <span data-ttu-id="1afda-137">Preparação</span><span class="sxs-lookup"><span data-stu-id="1afda-137">Staging</span></span> 

<span data-ttu-id="1afda-138">O valor padrão é produção.</span><span class="sxs-lookup"><span data-stu-id="1afda-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afda-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="1afda-139">-SubnetName</span></span>
<span data-ttu-id="1afda-140">Especifica o nome de uma sub-rede para a qual esse cmdlet associa o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="1afda-140">Specifies the name of a subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afda-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1afda-141">-VirtualNetworkName</span></span>
<span data-ttu-id="1afda-142">Especifica o nome de uma rede virtual que contém a sub-rede para a qual esse cmdlet associa o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="1afda-142">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afda-143">-VM</span><span class="sxs-lookup"><span data-stu-id="1afda-143">-VM</span></span>
<span data-ttu-id="1afda-144">Especifica a máquina virtual para a qual esse cmdlet aplica o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="1afda-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1afda-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1afda-145">CommonParameters</span></span>
<span data-ttu-id="1afda-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1afda-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1afda-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1afda-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1afda-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1afda-148">INPUTS</span></span>

## <span data-ttu-id="1afda-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1afda-149">OUTPUTS</span></span>

### <span data-ttu-id="1afda-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1afda-150">System.Boolean</span></span>

## <span data-ttu-id="1afda-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1afda-151">NOTES</span></span>

## <span data-ttu-id="1afda-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1afda-152">RELATED LINKS</span></span>

[<span data-ttu-id="1afda-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="1afda-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="1afda-154">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="1afda-154">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)


