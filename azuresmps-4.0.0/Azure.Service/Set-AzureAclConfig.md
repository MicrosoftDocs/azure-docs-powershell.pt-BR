---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946432"
---
# <span data-ttu-id="6d924-101">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="6d924-101">Set-AzureAclConfig</span></span>

## <span data-ttu-id="6d924-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d924-102">SYNOPSIS</span></span>
<span data-ttu-id="6d924-103">Modifica um objeto de configuração de ACL.</span><span class="sxs-lookup"><span data-stu-id="6d924-103">Modifies an ACL configuration object.</span></span>

## <span data-ttu-id="6d924-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d924-104">SYNTAX</span></span>

### <span data-ttu-id="6d924-105">Addrule</span><span class="sxs-lookup"><span data-stu-id="6d924-105">AddRule</span></span>
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6d924-106">RemoveRule</span><span class="sxs-lookup"><span data-stu-id="6d924-106">RemoveRule</span></span>
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6d924-107">SetRule</span><span class="sxs-lookup"><span data-stu-id="6d924-107">SetRule</span></span>
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6d924-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d924-108">DESCRIPTION</span></span>
<span data-ttu-id="6d924-109">O cmdlet **set-AzureAclConfig** modifica um objeto de configuração de ACL (lista de controle de acesso) de uma configuração de máquina virtual do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="6d924-109">The **Set-AzureAclConfig** cmdlet modifies an access control list (ACL) configuration object from an existing Azure virtual machine configuration.</span></span>

## <span data-ttu-id="6d924-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d924-110">EXAMPLES</span></span>

### <span data-ttu-id="6d924-111">Exemplo 1: adicionar uma regra a uma nova configuração de ACL</span><span class="sxs-lookup"><span data-stu-id="6d924-111">Example 1: Add a rule to a new ACL configuration</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

<span data-ttu-id="6d924-112">O primeiro comando cria uma configuração de ACL e armazena-a na variável $Acl.</span><span class="sxs-lookup"><span data-stu-id="6d924-112">The first command creates an ACL configuration, and then stores it in the $Acl variable.</span></span>

<span data-ttu-id="6d924-113">O segundo comando adiciona uma nova regra à configuração armazenada em $Acl.</span><span class="sxs-lookup"><span data-stu-id="6d924-113">The second command adds a new rule to the configuration stored in $Acl.</span></span>
<span data-ttu-id="6d924-114">O comando especifica uma ação, uma sub-rede, uma ordem e uma descrição para a regra.</span><span class="sxs-lookup"><span data-stu-id="6d924-114">The command specifies an action, subnet, order, and description for the rule.</span></span>

### <span data-ttu-id="6d924-115">Exemplo 2: modificar uma regra em uma configuração de ACL</span><span class="sxs-lookup"><span data-stu-id="6d924-115">Example 2: Modify a rule in an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="6d924-116">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 no serviço chamado ContosoService usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="6d924-116">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="6d924-117">O comando passa esse objeto para o cmdlet **Get-AzureAclConfig** usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="6d924-117">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6d924-118">Esse cmdlet obtém a configuração de ACL para o ponto de extremidade chamado Web.</span><span class="sxs-lookup"><span data-stu-id="6d924-118">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="6d924-119">O comando armazena esse objeto de configuração de ACL na variável $Acl.</span><span class="sxs-lookup"><span data-stu-id="6d924-119">The command stores that ACL configuration object in the $Acl variable.</span></span>

<span data-ttu-id="6d924-120">O segundo comando modifica a regra que tem a ID 0.</span><span class="sxs-lookup"><span data-stu-id="6d924-120">The second command modifies the rule that has the ID of 0.</span></span>
<span data-ttu-id="6d924-121">O comando altera o pedido e a descrição da regra.</span><span class="sxs-lookup"><span data-stu-id="6d924-121">The command changes the order and the description of the rule.</span></span>

<span data-ttu-id="6d924-122">O comando final define o objeto de configuração ACL para essa máquina virtual usando o cmdlet **set-AzureEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="6d924-122">The final command sets the ACL configuration object for that virtual machine by using the **Set-AzureEndpoint** cmdlet.</span></span>
<span data-ttu-id="6d924-123">O comando também atualiza essa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6d924-123">The command also updates that virtual machine.</span></span>

### <span data-ttu-id="6d924-124">Exemplo 3: remover uma regra de uma configuração de ACL</span><span class="sxs-lookup"><span data-stu-id="6d924-124">Example 3: Remove a rule from an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="6d924-125">O primeiro comando armazena um objeto de configuração ACL na variável $Acl.</span><span class="sxs-lookup"><span data-stu-id="6d924-125">The first command stores an ACL configuration object in the $Acl variable.</span></span>
<span data-ttu-id="6d924-126">Isso é o mesmo que o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="6d924-126">This is the same as the previous example.</span></span>

<span data-ttu-id="6d924-127">O segundo comando Remove a regra que tem a ID 0 da configuração de ACL em $Acl.</span><span class="sxs-lookup"><span data-stu-id="6d924-127">The second command removes the rule that has the ID 0 from the ACL configuration in $Acl.</span></span>

<span data-ttu-id="6d924-128">O comando final define o objeto de configuração de ACL para a máquina virtual e atualiza a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6d924-128">The final command sets the ACL configuration object for the virtual machine and updates that virtual machine.</span></span>
<span data-ttu-id="6d924-129">Isso é o mesmo que o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="6d924-129">This is the same as the previous example.</span></span>

## <span data-ttu-id="6d924-130">OS</span><span class="sxs-lookup"><span data-stu-id="6d924-130">PARAMETERS</span></span>

### <span data-ttu-id="6d924-131">-ACL</span><span class="sxs-lookup"><span data-stu-id="6d924-131">-ACL</span></span>
<span data-ttu-id="6d924-132">Especifica um objeto de configuração de ACL que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="6d924-132">Specifies an ACL configuration object that this cmdlet modifies.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d924-133">-Ação</span><span class="sxs-lookup"><span data-stu-id="6d924-133">-Action</span></span>
<span data-ttu-id="6d924-134">Especifica a ação para a regra que este cmdlet adiciona ou modifica.</span><span class="sxs-lookup"><span data-stu-id="6d924-134">Specifies the action for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="6d924-135">Os valores válidos são: Permit e Deny.</span><span class="sxs-lookup"><span data-stu-id="6d924-135">Valid values are: Permit and Deny.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d924-136">-Addrule</span><span class="sxs-lookup"><span data-stu-id="6d924-136">-AddRule</span></span>
<span data-ttu-id="6d924-137">Indica que esse cmdlet adiciona uma regra à configuração de ACL.</span><span class="sxs-lookup"><span data-stu-id="6d924-137">Indicates that this cmdlet adds a rule to the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d924-138">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6d924-138">-Description</span></span>
<span data-ttu-id="6d924-139">Especifica uma descrição para a regra que este cmdlet adiciona ou modifica.</span><span class="sxs-lookup"><span data-stu-id="6d924-139">Specifies a description for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d924-140">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="6d924-140">-InformationAction</span></span>
<span data-ttu-id="6d924-141">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="6d924-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6d924-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6d924-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d924-143">Contínuo</span><span class="sxs-lookup"><span data-stu-id="6d924-143">Continue</span></span>
- <span data-ttu-id="6d924-144">Ignorar</span><span class="sxs-lookup"><span data-stu-id="6d924-144">Ignore</span></span>
- <span data-ttu-id="6d924-145">Inquire</span><span class="sxs-lookup"><span data-stu-id="6d924-145">Inquire</span></span>
- <span data-ttu-id="6d924-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6d924-146">SilentlyContinue</span></span>
- <span data-ttu-id="6d924-147">Finaliza</span><span class="sxs-lookup"><span data-stu-id="6d924-147">Stop</span></span>
- <span data-ttu-id="6d924-148">Suspensão</span><span class="sxs-lookup"><span data-stu-id="6d924-148">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d924-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6d924-149">-InformationVariable</span></span>
<span data-ttu-id="6d924-150">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="6d924-150">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d924-151">-Pedido</span><span class="sxs-lookup"><span data-stu-id="6d924-151">-Order</span></span>
<span data-ttu-id="6d924-152">Especifica a ordem de processamento para a regra que este cmdlet adiciona ou modifica.</span><span class="sxs-lookup"><span data-stu-id="6d924-152">Specifies the processing order for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d924-153">-RemoteSubnet</span><span class="sxs-lookup"><span data-stu-id="6d924-153">-RemoteSubnet</span></span>
<span data-ttu-id="6d924-154">Especifica a sub-rede remota para a regra que este cmdlet adiciona ou modifica.</span><span class="sxs-lookup"><span data-stu-id="6d924-154">Specifies the remote subnet for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="6d924-155">Especifica um endereço no formato CIDR (roteamento interdomínio sem classe).</span><span class="sxs-lookup"><span data-stu-id="6d924-155">Specifies an address in Classless Interdomain Routing (CIDR) format.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d924-156">-RemoveRule</span><span class="sxs-lookup"><span data-stu-id="6d924-156">-RemoveRule</span></span>
<span data-ttu-id="6d924-157">Indica que esse cmdlet Remove uma regra da configuração de ACL.</span><span class="sxs-lookup"><span data-stu-id="6d924-157">Indicates that this cmdlet removes a rule from the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d924-158">-RuleId</span><span class="sxs-lookup"><span data-stu-id="6d924-158">-RuleId</span></span>
<span data-ttu-id="6d924-159">Especifica a ID da regra que este cmdlet Remove ou modifica para a configuração de ACL.</span><span class="sxs-lookup"><span data-stu-id="6d924-159">Specifies the ID of the rule that this cmdlet removes or modifies for the ACL configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d924-160">-SetRule</span><span class="sxs-lookup"><span data-stu-id="6d924-160">-SetRule</span></span>
<span data-ttu-id="6d924-161">Indica que esse cmdlet modifica uma regra na configuração de ACL.</span><span class="sxs-lookup"><span data-stu-id="6d924-161">Indicates that this cmdlet modifies a rule in the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d924-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d924-162">CommonParameters</span></span>
<span data-ttu-id="6d924-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d924-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d924-164">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d924-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d924-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d924-165">INPUTS</span></span>

## <span data-ttu-id="6d924-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d924-166">OUTPUTS</span></span>

## <span data-ttu-id="6d924-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d924-167">NOTES</span></span>

## <span data-ttu-id="6d924-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d924-168">RELATED LINKS</span></span>

[<span data-ttu-id="6d924-169">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="6d924-169">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="6d924-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6d924-170">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="6d924-171">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="6d924-171">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="6d924-172">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="6d924-172">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="6d924-173">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="6d924-173">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="6d924-174">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6d924-174">Update-AzureVM</span></span>](./Update-AzureVM.md)


