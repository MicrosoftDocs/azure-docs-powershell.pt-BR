---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112258"
---
# <span data-ttu-id="0203c-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0203c-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="0203c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0203c-102">SYNOPSIS</span></span>
<span data-ttu-id="0203c-103">Registra uma máquina virtual do Azure executando o sistema operacional Windows como um nó DSC para uma conta de Automação.</span><span class="sxs-lookup"><span data-stu-id="0203c-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="0203c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0203c-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0203c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0203c-105">DESCRIPTION</span></span>
<span data-ttu-id="0203c-106">O cmdlet **Register-AzAutomationDscNode** registra uma máquina virtual do Azure como um nó DSC (Configuração de Estado Desejado) APS em uma conta de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0203c-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="0203c-107">Este cmdlet registrará apenas VMs executando o sistema operacional Windows como um Nó DSC de automação para uma conta.</span><span class="sxs-lookup"><span data-stu-id="0203c-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="0203c-108">Se precisar registrar um nó em uma conta de automação em uma assinatura diferente, você precisará usar um modelo ARM em vez de cmdlets.</span><span class="sxs-lookup"><span data-stu-id="0203c-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="0203c-109">Consulte a documentação de Automação [do](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) Azure para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="0203c-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="0203c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0203c-110">EXAMPLES</span></span>

### <span data-ttu-id="0203c-111">Exemplo 1: Registrar uma máquina virtual do Azure como um nó DSC do Azure</span><span class="sxs-lookup"><span data-stu-id="0203c-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="0203c-112">Esse comando registra a máquina virtual do Azure chamada VirtualMachine01 como um nó DSC na conta automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0203c-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0203c-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0203c-113">PARAMETERS</span></span>

### <span data-ttu-id="0203c-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="0203c-114">-ActionAfterReboot</span></span>
<span data-ttu-id="0203c-115">Especifica a ação que a máquina virtual toma depois que ela é reiniciada.</span><span class="sxs-lookup"><span data-stu-id="0203c-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="0203c-116">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="0203c-116">Valid values are:</span></span> 
- <span data-ttu-id="0203c-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="0203c-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="0203c-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="0203c-118">StopConfiguration</span></span>

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

### <span data-ttu-id="0203c-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="0203c-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="0203c-120">Especifica se as novas configurações que esse nó DSC baixa do servidor de pull do Azure Automation DSC substituem os módulos existentes que já estão no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="0203c-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="0203c-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0203c-121">-AutomationAccountName</span></span>
<span data-ttu-id="0203c-122">Especifica o nome de uma conta de Automação na qual este cmdlet registra uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0203c-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="0203c-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="0203c-123">-AzureVMLocation</span></span>
<span data-ttu-id="0203c-124">O local do VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="0203c-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="0203c-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="0203c-125">-AzureVMName</span></span>
<span data-ttu-id="0203c-126">O nome da máquina virtual do Azure para se registrar para gerenciamento com o DSC de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0203c-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="0203c-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0203c-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="0203c-128">O nome do grupo de recursos VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="0203c-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="0203c-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="0203c-129">-ConfigurationMode</span></span>
<span data-ttu-id="0203c-130">Especifica o modo de configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="0203c-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="0203c-131">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="0203c-131">Valid values are:</span></span> 
- <span data-ttu-id="0203c-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="0203c-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="0203c-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="0203c-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="0203c-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="0203c-134">ApplyOnly</span></span>

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

### <span data-ttu-id="0203c-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="0203c-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="0203c-136">Especifica a frequência, em minutos, na qual o aplicativo de plano de fundo do DSC tenta implementar a configuração atual no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="0203c-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="0203c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0203c-137">-DefaultProfile</span></span>
<span data-ttu-id="0203c-138">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0203c-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0203c-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0203c-139">-NodeConfigurationName</span></span>
<span data-ttu-id="0203c-140">Especifica o nome da configuração do nó que esse cmdlet configura a máquina virtual a ser puxada do DSC de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0203c-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="0203c-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="0203c-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="0203c-142">Especifica se a máquina virtual deve ser reiniciada, se necessário.</span><span class="sxs-lookup"><span data-stu-id="0203c-142">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="0203c-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="0203c-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="0203c-144">Especifica a frequência, em minutos, na qual o Gerenciador de Configurações local contata o servidor de pull do Azure Automation DSC para baixar a configuração de nó mais recente.</span><span class="sxs-lookup"><span data-stu-id="0203c-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="0203c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0203c-145">-ResourceGroupName</span></span>
<span data-ttu-id="0203c-146">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0203c-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0203c-147">A conta automação com a qual esse cmdlet registra uma máquina virtual pertence ao grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0203c-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0203c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0203c-148">CommonParameters</span></span>
<span data-ttu-id="0203c-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0203c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0203c-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0203c-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0203c-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="0203c-151">INPUTS</span></span>

### <span data-ttu-id="0203c-152">System.String</span><span class="sxs-lookup"><span data-stu-id="0203c-152">System.String</span></span>

### <span data-ttu-id="0203c-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0203c-153">System.Int32</span></span>

### <span data-ttu-id="0203c-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0203c-154">System.Boolean</span></span>

## <span data-ttu-id="0203c-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="0203c-155">OUTPUTS</span></span>

### <span data-ttu-id="0203c-156">System.Void</span><span class="sxs-lookup"><span data-stu-id="0203c-156">System.Void</span></span>

## <span data-ttu-id="0203c-157">Notas</span><span class="sxs-lookup"><span data-stu-id="0203c-157">NOTES</span></span>

## <span data-ttu-id="0203c-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0203c-158">RELATED LINKS</span></span>

[<span data-ttu-id="0203c-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0203c-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="0203c-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0203c-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="0203c-161">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0203c-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


