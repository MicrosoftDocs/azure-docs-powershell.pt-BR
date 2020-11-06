---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 8abd6859054245c6265cc32695fa56168aabd1c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597880"
---
# <span data-ttu-id="ccb56-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ccb56-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="ccb56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccb56-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb56-103">Exporta uma configuração DSC da automação para um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="ccb56-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="ccb56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccb56-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccb56-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ccb56-105">DESCRIPTION</span></span>
<span data-ttu-id="ccb56-106">O cmdlet **Export-AzAutomationDscConfiguration** exporta uma configuração de estado desejado do APS (DSC) da automação do Azure para um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="ccb56-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="ccb56-107">O arquivo exportado tem uma extensão de nome de arquivo. ps1.</span><span class="sxs-lookup"><span data-stu-id="ccb56-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="ccb56-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ccb56-108">EXAMPLES</span></span>

### <span data-ttu-id="ccb56-109">Exemplo 1: exportar a versão publicada de uma configuração DSC</span><span class="sxs-lookup"><span data-stu-id="ccb56-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="ccb56-110">Esse comando exporta a versão publicada de uma configuração DSC na automação para a pasta especificada, que é a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ccb56-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="ccb56-111">OS</span><span class="sxs-lookup"><span data-stu-id="ccb56-111">PARAMETERS</span></span>

### <span data-ttu-id="ccb56-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ccb56-112">-AutomationAccountName</span></span>
<span data-ttu-id="ccb56-113">Especifica o nome da conta de automação que contém o DSC que este cmdlet exporta.</span><span class="sxs-lookup"><span data-stu-id="ccb56-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="ccb56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccb56-114">-DefaultProfile</span></span>
<span data-ttu-id="ccb56-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ccb56-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccb56-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ccb56-116">-Force</span></span>
<span data-ttu-id="ccb56-117">Indica que esse cmdlet substitui um arquivo local existente por um novo arquivo que tem o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="ccb56-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="ccb56-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccb56-118">-Name</span></span>
<span data-ttu-id="ccb56-119">Especifica o nome da configuração DSC que este cmdlet exporta.</span><span class="sxs-lookup"><span data-stu-id="ccb56-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="ccb56-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="ccb56-120">-OutputFolder</span></span>
<span data-ttu-id="ccb56-121">Especifica a pasta de saída em que esse cmdlet exporta a configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="ccb56-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="ccb56-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccb56-122">-ResourceGroupName</span></span>
<span data-ttu-id="ccb56-123">Especifica o nome de um grupo de recursos para o qual esse cmdlet exporta uma configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="ccb56-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="ccb56-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="ccb56-124">-Slot</span></span>
<span data-ttu-id="ccb56-125">Especifica qual versão da configuração DSC é exportada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccb56-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="ccb56-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="ccb56-126">Valid values are:</span></span> 
- <span data-ttu-id="ccb56-127">Provisório</span><span class="sxs-lookup"><span data-stu-id="ccb56-127">Draft</span></span>
- <span data-ttu-id="ccb56-128">Publicado o valor padrão é publicado.</span><span class="sxs-lookup"><span data-stu-id="ccb56-128">Published The default value is Published.</span></span>

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

### <span data-ttu-id="ccb56-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ccb56-129">-Confirm</span></span>
<span data-ttu-id="ccb56-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccb56-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccb56-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccb56-131">-WhatIf</span></span>
<span data-ttu-id="ccb56-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ccb56-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccb56-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ccb56-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccb56-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb56-134">CommonParameters</span></span>
<span data-ttu-id="ccb56-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccb56-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb56-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccb56-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb56-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ccb56-137">INPUTS</span></span>

### <span data-ttu-id="ccb56-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ccb56-138">System.String</span></span>

## <span data-ttu-id="ccb56-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ccb56-139">OUTPUTS</span></span>

### <span data-ttu-id="ccb56-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="ccb56-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="ccb56-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ccb56-141">NOTES</span></span>

## <span data-ttu-id="ccb56-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccb56-142">RELATED LINKS</span></span>

[<span data-ttu-id="ccb56-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ccb56-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="ccb56-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ccb56-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


