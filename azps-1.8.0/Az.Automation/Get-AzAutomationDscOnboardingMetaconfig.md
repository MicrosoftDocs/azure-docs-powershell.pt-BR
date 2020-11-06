---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 0302803568bac71baed28615552848f113da32df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601620"
---
# <span data-ttu-id="7056e-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="7056e-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="7056e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7056e-102">SYNOPSIS</span></span>
<span data-ttu-id="7056e-103">Cria arquivos de meta-configuração. mof.</span><span class="sxs-lookup"><span data-stu-id="7056e-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="7056e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7056e-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7056e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7056e-105">DESCRIPTION</span></span>
<span data-ttu-id="7056e-106">O cmdlet **Get-AzAutomationDscOnboardingMetaconfig** cria os arquivos MOF (formato de objeto gerenciado) de metadados de configuração de estado desejado do APS (MOF).</span><span class="sxs-lookup"><span data-stu-id="7056e-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="7056e-107">Esse cmdlet cria um arquivo. MOF para cada nome de computador que você especificar.</span><span class="sxs-lookup"><span data-stu-id="7056e-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="7056e-108">O cmdlet cria uma pasta para os arquivos. mof.</span><span class="sxs-lookup"><span data-stu-id="7056e-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="7056e-109">Você pode executar o cmdlet Set-DscLocalConfigurationManager para esta pasta para integrar esses computadores em uma conta de automação do Azure como nós DSC.</span><span class="sxs-lookup"><span data-stu-id="7056e-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="7056e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7056e-110">EXAMPLES</span></span>

### <span data-ttu-id="7056e-111">Exemplo 1: servidores onboard para DSC de automação</span><span class="sxs-lookup"><span data-stu-id="7056e-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="7056e-112">O primeiro comando cria arquivos de metaconfiguração DSC para dois servidores para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7056e-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="7056e-113">O comando salva esses arquivos em uma área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7056e-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="7056e-114">O segundo comando usa o cmdlet **set-DscLocalConfigurationManager** para aplicar a meta-configuração aos computadores especificados para que fiquem integradas como nós DSC.</span><span class="sxs-lookup"><span data-stu-id="7056e-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="7056e-115">OS</span><span class="sxs-lookup"><span data-stu-id="7056e-115">PARAMETERS</span></span>

### <span data-ttu-id="7056e-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7056e-116">-AutomationAccountName</span></span>
<span data-ttu-id="7056e-117">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="7056e-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="7056e-118">Você pode embutir os computadores que o parâmetro *ComputerName* especifica para a conta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7056e-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="7056e-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="7056e-119">-ComputerName</span></span>
<span data-ttu-id="7056e-120">Especifica uma matriz de nomes de computadores para os quais esse cmdlet gera arquivos. mof.</span><span class="sxs-lookup"><span data-stu-id="7056e-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="7056e-121">Se você não especificar esse parâmetro, o cmdlet gerará um arquivo. MOF para o computador atual (localhost).</span><span class="sxs-lookup"><span data-stu-id="7056e-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7056e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7056e-122">-DefaultProfile</span></span>
<span data-ttu-id="7056e-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7056e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7056e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7056e-124">-Force</span></span>
<span data-ttu-id="7056e-125">Força o comando a ser executado sem solicitar confirmação e substituir arquivos. mof existentes que tenham o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="7056e-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="7056e-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="7056e-126">-OutputFolder</span></span>
<span data-ttu-id="7056e-127">Especifica o nome de uma pasta onde esse cmdlet armazena arquivos. mof.</span><span class="sxs-lookup"><span data-stu-id="7056e-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

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

### <span data-ttu-id="7056e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7056e-128">-ResourceGroupName</span></span>
<span data-ttu-id="7056e-129">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7056e-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7056e-130">Esse cmdlet cria arquivos. MOF para computadores onboard no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7056e-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7056e-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7056e-131">-Confirm</span></span>
<span data-ttu-id="7056e-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7056e-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7056e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7056e-133">-WhatIf</span></span>
<span data-ttu-id="7056e-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7056e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7056e-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7056e-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7056e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7056e-136">CommonParameters</span></span>
<span data-ttu-id="7056e-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7056e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7056e-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7056e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7056e-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7056e-139">INPUTS</span></span>

### <span data-ttu-id="7056e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7056e-140">System.String</span></span>

### <span data-ttu-id="7056e-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="7056e-141">System.String[]</span></span>

## <span data-ttu-id="7056e-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7056e-142">OUTPUTS</span></span>

### <span data-ttu-id="7056e-143">Microsoft. Azure. Commands. Automation. Model. DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="7056e-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="7056e-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7056e-144">NOTES</span></span>

## <span data-ttu-id="7056e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7056e-145">RELATED LINKS</span></span>
