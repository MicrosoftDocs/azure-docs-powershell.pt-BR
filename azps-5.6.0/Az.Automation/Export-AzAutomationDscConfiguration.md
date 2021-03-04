---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: c27f878d2dbb0e52a16216a2158c737bc523c932
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886265"
---
# <span data-ttu-id="70648-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="70648-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="70648-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70648-102">SYNOPSIS</span></span>
<span data-ttu-id="70648-103">Exporta uma configuração DSC da Automação para um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="70648-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="70648-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="70648-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70648-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="70648-105">DESCRIPTION</span></span>
<span data-ttu-id="70648-106">O cmdlet **Export-AzAutomationDscConfiguration** exporta uma configuração de Estado Desejado (DSC) do APS da Automação do Azure para um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="70648-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="70648-107">O arquivo exportado tem uma extensão de nome de arquivo .ps1.</span><span class="sxs-lookup"><span data-stu-id="70648-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="70648-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70648-108">EXAMPLES</span></span>

### <span data-ttu-id="70648-109">Exemplo 1: Exportar a versão publicada de uma configuração DSC</span><span class="sxs-lookup"><span data-stu-id="70648-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="70648-110">Este comando exporta a versão publicada de uma configuração DSC em Automação para a pasta especificada, que é a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="70648-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="70648-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="70648-111">PARAMETERS</span></span>

### <span data-ttu-id="70648-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="70648-112">-AutomationAccountName</span></span>
<span data-ttu-id="70648-113">Especifica o nome da conta de automação que contém o DSC que esse cmdlet exporta.</span><span class="sxs-lookup"><span data-stu-id="70648-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="70648-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70648-114">-DefaultProfile</span></span>
<span data-ttu-id="70648-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="70648-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70648-116">-Force</span><span class="sxs-lookup"><span data-stu-id="70648-116">-Force</span></span>
<span data-ttu-id="70648-117">Indica que esse cmdlet substitui um arquivo local existente por um novo arquivo com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="70648-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="70648-118">-Name</span><span class="sxs-lookup"><span data-stu-id="70648-118">-Name</span></span>
<span data-ttu-id="70648-119">Especifica o nome da configuração DSC que esse cmdlet exporta.</span><span class="sxs-lookup"><span data-stu-id="70648-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70648-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="70648-120">-OutputFolder</span></span>
<span data-ttu-id="70648-121">Especifica a pasta de saída onde esse cmdlet exporta a configuração do DSC.</span><span class="sxs-lookup"><span data-stu-id="70648-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="70648-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70648-122">-ResourceGroupName</span></span>
<span data-ttu-id="70648-123">Especifica o nome de um grupo de recursos para o qual esse cmdlet exporta uma configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="70648-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="70648-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="70648-124">-Slot</span></span>
<span data-ttu-id="70648-125">Especifica qual versão da configuração do DSC que esse cmdlet exporta.</span><span class="sxs-lookup"><span data-stu-id="70648-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="70648-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="70648-126">Valid values are:</span></span> 
- <span data-ttu-id="70648-127">Rascunho</span><span class="sxs-lookup"><span data-stu-id="70648-127">Draft</span></span>
- <span data-ttu-id="70648-128">Publicado O valor padrão é Publicado.</span><span class="sxs-lookup"><span data-stu-id="70648-128">Published The default value is Published.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70648-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70648-129">-Confirm</span></span>
<span data-ttu-id="70648-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70648-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70648-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70648-131">-WhatIf</span></span>
<span data-ttu-id="70648-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="70648-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70648-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70648-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70648-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70648-134">CommonParameters</span></span>
<span data-ttu-id="70648-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70648-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70648-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70648-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70648-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70648-137">INPUTS</span></span>

### <span data-ttu-id="70648-138">System.String</span><span class="sxs-lookup"><span data-stu-id="70648-138">System.String</span></span>

## <span data-ttu-id="70648-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="70648-139">OUTPUTS</span></span>

### <span data-ttu-id="70648-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="70648-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="70648-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="70648-141">NOTES</span></span>

## <span data-ttu-id="70648-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70648-142">RELATED LINKS</span></span>

[<span data-ttu-id="70648-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="70648-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="70648-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="70648-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


