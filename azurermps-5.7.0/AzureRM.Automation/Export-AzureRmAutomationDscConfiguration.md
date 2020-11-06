---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 2f739c9471e2a6144c12033ade885a445bade12e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610134"
---
# <span data-ttu-id="6e87e-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e87e-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="6e87e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e87e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e87e-103">Exporta uma configuração DSC da automação para um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="6e87e-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e87e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e87e-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e87e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e87e-105">DESCRIPTION</span></span>
<span data-ttu-id="6e87e-106">O cmdlet **Export-AzureRmAutomationDscConfiguration** exporta uma configuração de estado desejado do APS (DSC) da automação do Azure para um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="6e87e-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="6e87e-107">O arquivo exportado tem uma extensão de nome de arquivo. ps1.</span><span class="sxs-lookup"><span data-stu-id="6e87e-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="6e87e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e87e-108">EXAMPLES</span></span>

### <span data-ttu-id="6e87e-109">Exemplo 1: exportar a versão publicada de uma configuração DSC</span><span class="sxs-lookup"><span data-stu-id="6e87e-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="6e87e-110">Esse comando exporta a versão publicada de uma configuração DSC na automação para a pasta especificada, que é a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6e87e-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="6e87e-111">OS</span><span class="sxs-lookup"><span data-stu-id="6e87e-111">PARAMETERS</span></span>

### <span data-ttu-id="6e87e-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6e87e-112">-AutomationAccountName</span></span>
<span data-ttu-id="6e87e-113">Especifica o nome da conta de automação que contém o DSC que este cmdlet exporta.</span><span class="sxs-lookup"><span data-stu-id="6e87e-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e87e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e87e-114">-DefaultProfile</span></span>
<span data-ttu-id="6e87e-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6e87e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6e87e-116">-Force</span></span>
<span data-ttu-id="6e87e-117">Indica que esse cmdlet substitui um arquivo local existente por um novo arquivo que tem o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="6e87e-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e87e-118">-Name</span></span>
<span data-ttu-id="6e87e-119">Especifica o nome da configuração DSC que este cmdlet exporta.</span><span class="sxs-lookup"><span data-stu-id="6e87e-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e87e-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="6e87e-120">-OutputFolder</span></span>
<span data-ttu-id="6e87e-121">Especifica a pasta de saída em que esse cmdlet exporta a configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="6e87e-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e87e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e87e-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e87e-123">Especifica o nome de um grupo de recursos para o qual esse cmdlet exporta uma configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="6e87e-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e87e-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="6e87e-124">-Slot</span></span>
<span data-ttu-id="6e87e-125">Especifica qual versão da configuração DSC é exportada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e87e-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="6e87e-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="6e87e-126">Valid values are:</span></span> 

- <span data-ttu-id="6e87e-127">Provisório</span><span class="sxs-lookup"><span data-stu-id="6e87e-127">Draft</span></span>
- <span data-ttu-id="6e87e-128">Publish</span><span class="sxs-lookup"><span data-stu-id="6e87e-128">Published</span></span> 

<span data-ttu-id="6e87e-129">O valor padrão é publicado.</span><span class="sxs-lookup"><span data-stu-id="6e87e-129">The default value is Published.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e87e-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6e87e-130">-Confirm</span></span>
<span data-ttu-id="6e87e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e87e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e87e-132">-WhatIf</span></span>
<span data-ttu-id="6e87e-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e87e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e87e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e87e-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e87e-135">CommonParameters</span></span>
<span data-ttu-id="6e87e-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e87e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e87e-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e87e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e87e-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e87e-138">INPUTS</span></span>

### <span data-ttu-id="6e87e-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6e87e-139">None</span></span>
<span data-ttu-id="6e87e-140">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6e87e-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6e87e-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e87e-141">OUTPUTS</span></span>

### <span data-ttu-id="6e87e-142">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="6e87e-142">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="6e87e-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e87e-143">NOTES</span></span>

## <span data-ttu-id="6e87e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e87e-144">RELATED LINKS</span></span>

[<span data-ttu-id="6e87e-145">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e87e-145">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="6e87e-146">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e87e-146">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


