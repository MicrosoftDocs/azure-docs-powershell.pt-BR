---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: ed35cf910dd0bf51803b6a38edc90a93f5411520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427002"
---
# <span data-ttu-id="b573d-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b573d-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="b573d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b573d-102">SYNOPSIS</span></span>
<span data-ttu-id="b573d-103">Exporta uma configuração DSC da automação para um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="b573d-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b573d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b573d-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b573d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b573d-105">DESCRIPTION</span></span>
<span data-ttu-id="b573d-106">O cmdlet **Export-AzureRmAutomationDscConfiguration** exporta uma configuração de estado desejado do APS (DSC) da automação do Azure para um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="b573d-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="b573d-107">O arquivo exportado tem uma extensão de nome de arquivo. ps1.</span><span class="sxs-lookup"><span data-stu-id="b573d-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="b573d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b573d-108">EXAMPLES</span></span>

### <span data-ttu-id="b573d-109">Exemplo 1: exportar a versão publicada de uma configuração DSC</span><span class="sxs-lookup"><span data-stu-id="b573d-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="b573d-110">Esse comando exporta a versão publicada de uma configuração DSC na automação para a pasta especificada, que é a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b573d-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="b573d-111">OS</span><span class="sxs-lookup"><span data-stu-id="b573d-111">PARAMETERS</span></span>

### <span data-ttu-id="b573d-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b573d-112">-AutomationAccountName</span></span>
<span data-ttu-id="b573d-113">Especifica o nome da conta de automação que contém o DSC que este cmdlet exporta.</span><span class="sxs-lookup"><span data-stu-id="b573d-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="b573d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b573d-114">-Force</span></span>
<span data-ttu-id="b573d-115">Indica que esse cmdlet substitui um arquivo local existente por um novo arquivo que tem o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="b573d-115">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="b573d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b573d-116">-Name</span></span>
<span data-ttu-id="b573d-117">Especifica o nome da configuração DSC que este cmdlet exporta.</span><span class="sxs-lookup"><span data-stu-id="b573d-117">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="b573d-118">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="b573d-118">-OutputFolder</span></span>
<span data-ttu-id="b573d-119">Especifica a pasta de saída em que esse cmdlet exporta a configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="b573d-119">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="b573d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b573d-120">-ResourceGroupName</span></span>
<span data-ttu-id="b573d-121">Especifica o nome de um grupo de recursos para o qual esse cmdlet exporta uma configuração DSC.</span><span class="sxs-lookup"><span data-stu-id="b573d-121">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="b573d-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="b573d-122">-Slot</span></span>
<span data-ttu-id="b573d-123">Especifica qual versão da configuração DSC é exportada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b573d-123">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="b573d-124">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b573d-124">Valid values are:</span></span> 

- <span data-ttu-id="b573d-125">Provisório</span><span class="sxs-lookup"><span data-stu-id="b573d-125">Draft</span></span>
- <span data-ttu-id="b573d-126">Publish</span><span class="sxs-lookup"><span data-stu-id="b573d-126">Published</span></span> 

<span data-ttu-id="b573d-127">O valor padrão é publicado.</span><span class="sxs-lookup"><span data-stu-id="b573d-127">The default value is Published.</span></span>

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

### <span data-ttu-id="b573d-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b573d-128">-Confirm</span></span>
<span data-ttu-id="b573d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b573d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b573d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b573d-130">-WhatIf</span></span>
<span data-ttu-id="b573d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b573d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b573d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b573d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b573d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b573d-133">-DefaultProfile</span></span>
<span data-ttu-id="b573d-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b573d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b573d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b573d-135">CommonParameters</span></span>
<span data-ttu-id="b573d-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b573d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b573d-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b573d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b573d-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b573d-138">INPUTS</span></span>

## <span data-ttu-id="b573d-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b573d-139">OUTPUTS</span></span>

### <span data-ttu-id="b573d-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="b573d-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="b573d-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b573d-141">NOTES</span></span>

## <span data-ttu-id="b573d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b573d-142">RELATED LINKS</span></span>

[<span data-ttu-id="b573d-143">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b573d-143">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="b573d-144">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b573d-144">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


