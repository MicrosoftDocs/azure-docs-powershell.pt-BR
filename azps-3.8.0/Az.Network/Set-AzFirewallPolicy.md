---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 1e5fbeba85431ab593d4daedff0f8b71af13ace4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942510"
---
# <span data-ttu-id="842df-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="842df-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="842df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="842df-102">SYNOPSIS</span></span>
<span data-ttu-id="842df-103">Salva uma política de firewall do Azure modificada</span><span class="sxs-lookup"><span data-stu-id="842df-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="842df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="842df-104">SYNTAX</span></span>

### <span data-ttu-id="842df-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="842df-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="842df-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="842df-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="842df-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="842df-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>] [-BasePolicy <String>]
 -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="842df-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="842df-108">DESCRIPTION</span></span>
<span data-ttu-id="842df-109">O cmdlet **set-AzFirewallPolicy** atualiza uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="842df-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="842df-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="842df-110">EXAMPLES</span></span>

### <span data-ttu-id="842df-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="842df-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="842df-112">Este exemplo define a política de firewall com o novo valor de política de firewall</span><span class="sxs-lookup"><span data-stu-id="842df-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="842df-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="842df-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="842df-114">Este exemplo define a política de firewall com o novo modo de ameaça Intel</span><span class="sxs-lookup"><span data-stu-id="842df-114">This example sets the firewall policy with the new threat intel mode</span></span>

## <span data-ttu-id="842df-115">OS</span><span class="sxs-lookup"><span data-stu-id="842df-115">PARAMETERS</span></span>

### <span data-ttu-id="842df-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="842df-116">-AsJob</span></span>
<span data-ttu-id="842df-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="842df-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842df-118">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="842df-118">-BasePolicy</span></span>
<span data-ttu-id="842df-119">A política base a ser herdada</span><span class="sxs-lookup"><span data-stu-id="842df-119">The base policy to inherit from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="842df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="842df-120">-DefaultProfile</span></span>
<span data-ttu-id="842df-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="842df-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842df-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="842df-122">-InputObject</span></span>
<span data-ttu-id="842df-123">A política AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="842df-123">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="842df-124">-Local</span><span class="sxs-lookup"><span data-stu-id="842df-124">-Location</span></span>
<span data-ttu-id="842df-125">ponto.</span><span class="sxs-lookup"><span data-stu-id="842df-125">location.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="842df-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="842df-126">-Name</span></span>
<span data-ttu-id="842df-127">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="842df-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="842df-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="842df-128">-ResourceGroupName</span></span>
<span data-ttu-id="842df-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="842df-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="842df-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="842df-130">-ResourceId</span></span>
<span data-ttu-id="842df-131">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="842df-131">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="842df-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="842df-132">-Tag</span></span>
<span data-ttu-id="842df-133">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="842df-133">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="842df-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="842df-134">-ThreatIntelMode</span></span>
<span data-ttu-id="842df-135">O modo de operação para inteligência de ameaças.</span><span class="sxs-lookup"><span data-stu-id="842df-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="842df-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="842df-136">-Confirm</span></span>
<span data-ttu-id="842df-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="842df-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842df-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="842df-138">-WhatIf</span></span>
<span data-ttu-id="842df-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="842df-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="842df-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="842df-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="842df-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="842df-141">CommonParameters</span></span>
<span data-ttu-id="842df-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="842df-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="842df-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="842df-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="842df-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="842df-144">INPUTS</span></span>

### <span data-ttu-id="842df-145">System. String</span><span class="sxs-lookup"><span data-stu-id="842df-145">System.String</span></span>

### <span data-ttu-id="842df-146">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="842df-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="842df-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="842df-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="842df-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="842df-148">OUTPUTS</span></span>

### <span data-ttu-id="842df-149">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="842df-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="842df-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="842df-150">NOTES</span></span>

## <span data-ttu-id="842df-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="842df-151">RELATED LINKS</span></span>
