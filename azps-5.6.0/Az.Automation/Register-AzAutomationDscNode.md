---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: ceae5a9e7dec9913d90aae836784c6bfe66b680f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892902"
---
# <span data-ttu-id="c48ea-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="c48ea-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="c48ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c48ea-102">SYNOPSIS</span></span>
<span data-ttu-id="c48ea-103">Registra uma máquina virtual do Azure executando o sistema operacional Windows como um nó DSC para uma conta de Automação.</span><span class="sxs-lookup"><span data-stu-id="c48ea-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="c48ea-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c48ea-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c48ea-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c48ea-105">DESCRIPTION</span></span>
<span data-ttu-id="c48ea-106">O cmdlet **Register-AzAutomationDscNode** registra uma máquina virtual do Azure como um nó DSC (Configuração de Estado Desejado) do APS em uma conta de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="c48ea-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="c48ea-107">Este cmdlet registrará apenas VMs que executam o sistema operacional Windows como um Nó DSC de Automação para uma conta.</span><span class="sxs-lookup"><span data-stu-id="c48ea-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="c48ea-108">Se você precisar registrar um nó em uma conta de automação em uma assinatura diferente, você precisará usar um modelo de ARM em vez de cmdlets.</span><span class="sxs-lookup"><span data-stu-id="c48ea-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="c48ea-109">Consulte a documentação de Automação [do](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) Azure para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="c48ea-109">See the Azure Automation [documentation](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="c48ea-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c48ea-110">EXAMPLES</span></span>

### <span data-ttu-id="c48ea-111">Exemplo 1: Registrar uma máquina virtual do Azure como um nó DSC do Azure</span><span class="sxs-lookup"><span data-stu-id="c48ea-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="c48ea-112">Esse comando registra a máquina virtual do Azure chamada VirtualMachine01 como um nó DSC na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c48ea-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c48ea-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c48ea-113">PARAMETERS</span></span>

### <span data-ttu-id="c48ea-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="c48ea-114">-ActionAfterReboot</span></span>
<span data-ttu-id="c48ea-115">Especifica a ação que a máquina virtual toma após a reinicialização.</span><span class="sxs-lookup"><span data-stu-id="c48ea-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="c48ea-116">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c48ea-116">Valid values are:</span></span> 
- <span data-ttu-id="c48ea-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="c48ea-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="c48ea-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="c48ea-118">StopConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48ea-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="c48ea-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="c48ea-120">Especifica se as novas configurações que esse nó DSC baixa do servidor pull do Azure Automation DSC substituem os módulos existentes já no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="c48ea-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48ea-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c48ea-121">-AutomationAccountName</span></span>
<span data-ttu-id="c48ea-122">Especifica o nome de uma conta de automação na qual esse cmdlet registra uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c48ea-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48ea-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="c48ea-123">-AzureVMLocation</span></span>
<span data-ttu-id="c48ea-124">O local da VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="c48ea-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="c48ea-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="c48ea-125">-AzureVMName</span></span>
<span data-ttu-id="c48ea-126">O nome da máquina virtual do Azure a ser registrado para gerenciamento com o Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="c48ea-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48ea-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c48ea-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="c48ea-128">O nome do grupo de recursos da VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="c48ea-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="c48ea-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="c48ea-129">-ConfigurationMode</span></span>
<span data-ttu-id="c48ea-130">Especifica o modo de configuração do DSC.</span><span class="sxs-lookup"><span data-stu-id="c48ea-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="c48ea-131">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c48ea-131">Valid values are:</span></span> 
- <span data-ttu-id="c48ea-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="c48ea-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="c48ea-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="c48ea-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="c48ea-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="c48ea-134">ApplyOnly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48ea-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="c48ea-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="c48ea-136">Especifica a frequência, em minutos, na qual o aplicativo em segundo plano do DSC tenta implementar a configuração atual no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="c48ea-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48ea-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48ea-137">-DefaultProfile</span></span>
<span data-ttu-id="c48ea-138">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c48ea-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c48ea-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c48ea-139">-NodeConfigurationName</span></span>
<span data-ttu-id="c48ea-140">Especifica o nome da configuração do nó que esse cmdlet configura a máquina virtual a ser puxada do Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="c48ea-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="c48ea-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="c48ea-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="c48ea-142">Especifica se a máquina virtual deve ser reiniciada, se necessário.</span><span class="sxs-lookup"><span data-stu-id="c48ea-142">Specifies whether to restart the virtual machine, if needed.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48ea-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="c48ea-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="c48ea-144">Especifica a frequência, em minutos, na qual o Gerenciador de Configurações local contata o servidor pull do Azure Automation DSC para baixar a configuração de nó mais recente.</span><span class="sxs-lookup"><span data-stu-id="c48ea-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48ea-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c48ea-145">-ResourceGroupName</span></span>
<span data-ttu-id="c48ea-146">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c48ea-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c48ea-147">A conta de automação com a qual esse cmdlet registra uma máquina virtual pertence ao grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c48ea-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48ea-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48ea-148">CommonParameters</span></span>
<span data-ttu-id="c48ea-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c48ea-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48ea-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c48ea-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48ea-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c48ea-151">INPUTS</span></span>

### <span data-ttu-id="c48ea-152">System.String</span><span class="sxs-lookup"><span data-stu-id="c48ea-152">System.String</span></span>

### <span data-ttu-id="c48ea-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c48ea-153">System.Int32</span></span>

### <span data-ttu-id="c48ea-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c48ea-154">System.Boolean</span></span>

## <span data-ttu-id="c48ea-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c48ea-155">OUTPUTS</span></span>

### <span data-ttu-id="c48ea-156">System.Void</span><span class="sxs-lookup"><span data-stu-id="c48ea-156">System.Void</span></span>

## <span data-ttu-id="c48ea-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="c48ea-157">NOTES</span></span>

## <span data-ttu-id="c48ea-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c48ea-158">RELATED LINKS</span></span>

[<span data-ttu-id="c48ea-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="c48ea-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="c48ea-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="c48ea-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="c48ea-161">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="c48ea-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


