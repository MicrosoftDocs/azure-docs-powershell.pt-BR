---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
ms.openlocfilehash: 1a0fd95df118e734ed594cf1efe35eb8f8476f50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431823"
---
# <span data-ttu-id="97dc8-101">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="97dc8-101">Register-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="97dc8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="97dc8-103">Registra uma máquina virtual do Azure como um nó DSC para uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="97dc8-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97dc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97dc8-104">SYNTAX</span></span>

```
Register-AzureRmAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97dc8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97dc8-105">DESCRIPTION</span></span>
<span data-ttu-id="97dc8-106">O cmdlet **Register-AzureRmAutomationDscNode** registra uma máquina virtual do Azure como um nó DSC (configuração de estado desejado APS) em uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="97dc8-106">The **Register-AzureRmAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="97dc8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97dc8-107">EXAMPLES</span></span>

### <span data-ttu-id="97dc8-108">Exemplo 1: registrar uma máquina virtual do Azure como um nó DSC do Azure</span><span class="sxs-lookup"><span data-stu-id="97dc8-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="97dc8-109">Esse comando registra a máquina virtual do Azure chamada VirtualMachine01 como um nó DSC na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="97dc8-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="97dc8-110">OS</span><span class="sxs-lookup"><span data-stu-id="97dc8-110">PARAMETERS</span></span>

### <span data-ttu-id="97dc8-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="97dc8-111">-ActionAfterReboot</span></span>
<span data-ttu-id="97dc8-112">Especifica a ação que a máquina virtual leva após ser reiniciada.</span><span class="sxs-lookup"><span data-stu-id="97dc8-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="97dc8-113">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="97dc8-113">Valid values are:</span></span> 

- <span data-ttu-id="97dc8-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="97dc8-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="97dc8-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="97dc8-115">StopConfiguration</span></span>

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

### <span data-ttu-id="97dc8-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="97dc8-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="97dc8-117">Especifica se as novas configurações que este nó DSC baixa do servidor de recebimento do DSC de automação do Azure substituem os módulos existentes que já estão no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="97dc8-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="97dc8-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="97dc8-118">-AutomationAccountName</span></span>
<span data-ttu-id="97dc8-119">Especifica o nome de uma conta de automação na qual esse cmdlet registra uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="97dc8-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="97dc8-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="97dc8-120">-AzureVMLocation</span></span>
<span data-ttu-id="97dc8-121">Especifica o local em que esse cmdlet registra uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="97dc8-121">Specifies the location in which this cmdlet registers a virtual machine.</span></span>
<span data-ttu-id="97dc8-122">Para obter locais válidos, use o cmdlet Get-AzureRMLocation.</span><span class="sxs-lookup"><span data-stu-id="97dc8-122">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="97dc8-123">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="97dc8-123">-AzureVMName</span></span>
<span data-ttu-id="97dc8-124">Especifica o nome da máquina virtual do Azure que este cmdlet registra para gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="97dc8-124">Specifies the name of the Azure virtual machine that this cmdlet registers for management.</span></span>

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

### <span data-ttu-id="97dc8-125">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="97dc8-125">-AzureVMResourceGroup</span></span>
<span data-ttu-id="97dc8-126">Especifica o nome do grupo de recursos da máquina virtual do Azure que este cmdlet registra.</span><span class="sxs-lookup"><span data-stu-id="97dc8-126">Specifies the name of the resource group of the Azure virtual machine that this cmdlet registers.</span></span>

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

### <span data-ttu-id="97dc8-127">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="97dc8-127">-ConfigurationMode</span></span>
<span data-ttu-id="97dc8-128">Especifica o modo de configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="97dc8-128">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="97dc8-129">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="97dc8-129">Valid values are:</span></span> 

- <span data-ttu-id="97dc8-130">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="97dc8-130">ApplyAndMonitor</span></span> 
- <span data-ttu-id="97dc8-131">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="97dc8-131">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="97dc8-132">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="97dc8-132">ApplyOnly</span></span>

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

### <span data-ttu-id="97dc8-133">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="97dc8-133">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="97dc8-134">Especifica a frequência, em minutos, em que o aplicativo em segundo plano do DSC tenta implementar a configuração atual no nó de destino.</span><span class="sxs-lookup"><span data-stu-id="97dc8-134">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="97dc8-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="97dc8-135">-NodeConfigurationName</span></span>
<span data-ttu-id="97dc8-136">Especifica o nome da configuração de nó que esse cmdlet configura a máquina virtual para extrair do DSC de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="97dc8-136">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="97dc8-137">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="97dc8-137">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="97dc8-138">Especifica se a máquina virtual deve ser reiniciada, se necessário.</span><span class="sxs-lookup"><span data-stu-id="97dc8-138">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="97dc8-139">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="97dc8-139">-RefreshFrequencyMins</span></span>
<span data-ttu-id="97dc8-140">Especifica a frequência, em minutos, em que o Gerenciador de configurações local contata o servidor pull do Azure Automation para baixar a configuração de nó mais recente.</span><span class="sxs-lookup"><span data-stu-id="97dc8-140">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="97dc8-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97dc8-141">-ResourceGroupName</span></span>
<span data-ttu-id="97dc8-142">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97dc8-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="97dc8-143">A conta de automação com a qual esse cmdlet registra uma máquina virtual pertence ao grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="97dc8-143">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="97dc8-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97dc8-144">-DefaultProfile</span></span>
<span data-ttu-id="97dc8-145">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97dc8-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97dc8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97dc8-146">CommonParameters</span></span>
<span data-ttu-id="97dc8-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97dc8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97dc8-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97dc8-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97dc8-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97dc8-149">INPUTS</span></span>

## <span data-ttu-id="97dc8-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97dc8-150">OUTPUTS</span></span>

## <span data-ttu-id="97dc8-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97dc8-151">NOTES</span></span>

## <span data-ttu-id="97dc8-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97dc8-152">RELATED LINKS</span></span>

[<span data-ttu-id="97dc8-153">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="97dc8-153">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="97dc8-154">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="97dc8-154">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="97dc8-155">Cancelar registro-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="97dc8-155">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


