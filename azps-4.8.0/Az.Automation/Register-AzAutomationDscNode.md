---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955158"
---
# <span data-ttu-id="0119c-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0119c-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="0119c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0119c-102">SYNOPSIS</span></span>
<span data-ttu-id="0119c-103">Registra uma máquina virtual do Azure executando o sistema operacional Windows como um nó DSC para uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="0119c-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="0119c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0119c-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0119c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0119c-105">DESCRIPTION</span></span>
<span data-ttu-id="0119c-106">O cmdlet **Register-AzAutomationDscNode** registra uma máquina virtual do Azure como um nó DSC (configuração de estado desejado APS) em uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0119c-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="0119c-107">Esse cmdlet somente registrará máquinas virtuais executando o sistema operacional Windows como um nó de DSC de automação para uma conta.</span><span class="sxs-lookup"><span data-stu-id="0119c-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="0119c-108">Se você precisar registrar um nó em uma conta de automação em uma assinatura diferente, será necessário usar um modelo ARM em vez de cmdlets.</span><span class="sxs-lookup"><span data-stu-id="0119c-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="0119c-109">Consulte a [documentação](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) de automação do Azure para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="0119c-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="0119c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0119c-110">EXAMPLES</span></span>

### <span data-ttu-id="0119c-111">Exemplo 1: registrar uma máquina virtual do Azure como um nó DSC do Azure</span><span class="sxs-lookup"><span data-stu-id="0119c-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="0119c-112">Esse comando registra a máquina virtual do Azure chamada VirtualMachine01 como um nó DSC na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0119c-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0119c-113">OS</span><span class="sxs-lookup"><span data-stu-id="0119c-113">PARAMETERS</span></span>

### <span data-ttu-id="0119c-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="0119c-114">-ActionAfterReboot</span></span>
<span data-ttu-id="0119c-115">Especifica a ação que a máquina virtual leva após ser reiniciada.</span><span class="sxs-lookup"><span data-stu-id="0119c-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="0119c-116">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="0119c-116">Valid values are:</span></span> 
- <span data-ttu-id="0119c-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="0119c-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="0119c-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="0119c-118">StopConfiguration</span></span>

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

### <span data-ttu-id="0119c-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="0119c-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="0119c-120">Especifica se as novas configurações que este nó DSC baixa do servidor de recebimento do DSC de automação do Azure substituem os módulos existentes que já estão no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="0119c-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="0119c-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0119c-121">-AutomationAccountName</span></span>
<span data-ttu-id="0119c-122">Especifica o nome de uma conta de automação na qual esse cmdlet registra uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0119c-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="0119c-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="0119c-123">-AzureVMLocation</span></span>
<span data-ttu-id="0119c-124">O local da VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="0119c-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="0119c-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="0119c-125">-AzureVMName</span></span>
<span data-ttu-id="0119c-126">O nome da máquina virtual do Azure para se registrar para gerenciamento com o DSC de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0119c-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="0119c-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0119c-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="0119c-128">O nome do grupo de recursos de VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="0119c-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="0119c-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="0119c-129">-ConfigurationMode</span></span>
<span data-ttu-id="0119c-130">Especifica o modo de configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="0119c-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="0119c-131">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="0119c-131">Valid values are:</span></span> 
- <span data-ttu-id="0119c-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="0119c-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="0119c-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="0119c-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="0119c-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="0119c-134">ApplyOnly</span></span>

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

### <span data-ttu-id="0119c-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="0119c-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="0119c-136">Especifica a frequência, em minutos, em que o aplicativo em segundo plano do DSC tenta implementar a configuração atual no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="0119c-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="0119c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0119c-137">-DefaultProfile</span></span>
<span data-ttu-id="0119c-138">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0119c-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0119c-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0119c-139">-NodeConfigurationName</span></span>
<span data-ttu-id="0119c-140">Especifica o nome da configuração de nó que esse cmdlet configura a máquina virtual para extrair do DSC de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="0119c-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="0119c-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="0119c-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="0119c-142">Especifica se a máquina virtual deve ser reiniciada, se necessário.</span><span class="sxs-lookup"><span data-stu-id="0119c-142">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="0119c-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="0119c-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="0119c-144">Especifica a frequência, em minutos, em que o Gerenciador de configurações local contata o servidor pull do Azure Automation para baixar a configuração de nó mais recente.</span><span class="sxs-lookup"><span data-stu-id="0119c-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="0119c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0119c-145">-ResourceGroupName</span></span>
<span data-ttu-id="0119c-146">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0119c-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0119c-147">A conta de automação com a qual esse cmdlet registra uma máquina virtual pertence ao grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="0119c-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0119c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0119c-148">CommonParameters</span></span>
<span data-ttu-id="0119c-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0119c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0119c-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0119c-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0119c-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0119c-151">INPUTS</span></span>

### <span data-ttu-id="0119c-152">System. String</span><span class="sxs-lookup"><span data-stu-id="0119c-152">System.String</span></span>

### <span data-ttu-id="0119c-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0119c-153">System.Int32</span></span>

### <span data-ttu-id="0119c-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0119c-154">System.Boolean</span></span>

## <span data-ttu-id="0119c-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0119c-155">OUTPUTS</span></span>

### <span data-ttu-id="0119c-156">System. void</span><span class="sxs-lookup"><span data-stu-id="0119c-156">System.Void</span></span>

## <span data-ttu-id="0119c-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0119c-157">NOTES</span></span>

## <span data-ttu-id="0119c-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0119c-158">RELATED LINKS</span></span>

[<span data-ttu-id="0119c-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0119c-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="0119c-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0119c-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="0119c-161">Cancelar registro-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0119c-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


