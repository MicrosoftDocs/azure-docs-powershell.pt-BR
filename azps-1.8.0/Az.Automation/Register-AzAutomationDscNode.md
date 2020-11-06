---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: 5dc2682597be6f05a65bafc38424139e9707578f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601548"
---
# <span data-ttu-id="3d97d-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3d97d-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="3d97d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d97d-102">SYNOPSIS</span></span>
<span data-ttu-id="3d97d-103">Registra uma máquina virtual do Azure como um nó DSC para uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="3d97d-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="3d97d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d97d-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d97d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d97d-105">DESCRIPTION</span></span>
<span data-ttu-id="3d97d-106">O cmdlet **Register-AzAutomationDscNode** registra uma máquina virtual do Azure como um nó DSC (configuração de estado desejado APS) em uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d97d-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="3d97d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d97d-107">EXAMPLES</span></span>

### <span data-ttu-id="3d97d-108">Exemplo 1: registrar uma máquina virtual do Azure como um nó DSC do Azure</span><span class="sxs-lookup"><span data-stu-id="3d97d-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="3d97d-109">Esse comando registra a máquina virtual do Azure chamada VirtualMachine01 como um nó DSC na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3d97d-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3d97d-110">OS</span><span class="sxs-lookup"><span data-stu-id="3d97d-110">PARAMETERS</span></span>

### <span data-ttu-id="3d97d-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="3d97d-111">-ActionAfterReboot</span></span>
<span data-ttu-id="3d97d-112">Especifica a ação que a máquina virtual leva após ser reiniciada.</span><span class="sxs-lookup"><span data-stu-id="3d97d-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="3d97d-113">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="3d97d-113">Valid values are:</span></span> 
- <span data-ttu-id="3d97d-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d97d-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="3d97d-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d97d-115">StopConfiguration</span></span>

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

### <span data-ttu-id="3d97d-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="3d97d-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="3d97d-117">Especifica se as novas configurações que este nó DSC baixa do servidor de recebimento do DSC de automação do Azure substituem os módulos existentes que já estão no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="3d97d-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="3d97d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3d97d-118">-AutomationAccountName</span></span>
<span data-ttu-id="3d97d-119">Especifica o nome de uma conta de automação na qual esse cmdlet registra uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3d97d-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="3d97d-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="3d97d-120">-AzureVMLocation</span></span>
<span data-ttu-id="3d97d-121">O local da VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d97d-121">The Azure VM location.</span></span>

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

### <span data-ttu-id="3d97d-122">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="3d97d-122">-AzureVMName</span></span>
<span data-ttu-id="3d97d-123">O nome da máquina virtual do Azure para se registrar para gerenciamento com o DSC de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d97d-123">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="3d97d-124">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3d97d-124">-AzureVMResourceGroup</span></span>
<span data-ttu-id="3d97d-125">O nome do grupo de recursos de VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d97d-125">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="3d97d-126">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="3d97d-126">-ConfigurationMode</span></span>
<span data-ttu-id="3d97d-127">Especifica o modo de configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="3d97d-127">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="3d97d-128">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="3d97d-128">Valid values are:</span></span> 
- <span data-ttu-id="3d97d-129">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="3d97d-129">ApplyAndMonitor</span></span> 
- <span data-ttu-id="3d97d-130">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="3d97d-130">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="3d97d-131">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="3d97d-131">ApplyOnly</span></span>

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

### <span data-ttu-id="3d97d-132">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="3d97d-132">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="3d97d-133">Especifica a frequência, em minutos, em que o aplicativo em segundo plano do DSC tenta implementar a configuração atual no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="3d97d-133">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="3d97d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d97d-134">-DefaultProfile</span></span>
<span data-ttu-id="3d97d-135">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3d97d-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d97d-136">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3d97d-136">-NodeConfigurationName</span></span>
<span data-ttu-id="3d97d-137">Especifica o nome da configuração de nó que esse cmdlet configura a máquina virtual para extrair do DSC de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d97d-137">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="3d97d-138">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="3d97d-138">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="3d97d-139">Especifica se a máquina virtual deve ser reiniciada, se necessário.</span><span class="sxs-lookup"><span data-stu-id="3d97d-139">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="3d97d-140">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="3d97d-140">-RefreshFrequencyMins</span></span>
<span data-ttu-id="3d97d-141">Especifica a frequência, em minutos, em que o Gerenciador de configurações local contata o servidor pull do Azure Automation para baixar a configuração de nó mais recente.</span><span class="sxs-lookup"><span data-stu-id="3d97d-141">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="3d97d-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d97d-142">-ResourceGroupName</span></span>
<span data-ttu-id="3d97d-143">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d97d-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3d97d-144">A conta de automação com a qual esse cmdlet registra uma máquina virtual pertence ao grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="3d97d-144">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d97d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d97d-145">CommonParameters</span></span>
<span data-ttu-id="3d97d-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d97d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d97d-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d97d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d97d-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d97d-148">INPUTS</span></span>

### <span data-ttu-id="3d97d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3d97d-149">System.String</span></span>

### <span data-ttu-id="3d97d-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3d97d-150">System.Int32</span></span>

### <span data-ttu-id="3d97d-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d97d-151">System.Boolean</span></span>

## <span data-ttu-id="3d97d-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d97d-152">OUTPUTS</span></span>

### <span data-ttu-id="3d97d-153">System. void</span><span class="sxs-lookup"><span data-stu-id="3d97d-153">System.Void</span></span>

## <span data-ttu-id="3d97d-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d97d-154">NOTES</span></span>

## <span data-ttu-id="3d97d-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d97d-155">RELATED LINKS</span></span>

[<span data-ttu-id="3d97d-156">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3d97d-156">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="3d97d-157">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3d97d-157">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="3d97d-158">Cancelar registro-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3d97d-158">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


