---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: c328dcbf912b5b907f0e27c902bc7eb3dc31a44e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427704"
---
# <span data-ttu-id="822dc-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="822dc-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="822dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="822dc-102">SYNOPSIS</span></span>
<span data-ttu-id="822dc-103">Remove as configurações DSC da automação.</span><span class="sxs-lookup"><span data-stu-id="822dc-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="822dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="822dc-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="822dc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="822dc-105">DESCRIPTION</span></span>
<span data-ttu-id="822dc-106">O cmdlet **Remove-AzureRmAutomationDscConfiguration** remove as configurações de estado desejado do APS (DSC) da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="822dc-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="822dc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="822dc-107">EXAMPLES</span></span>

## <span data-ttu-id="822dc-108">OS</span><span class="sxs-lookup"><span data-stu-id="822dc-108">PARAMETERS</span></span>

### <span data-ttu-id="822dc-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="822dc-109">-AutomationAccountName</span></span>
<span data-ttu-id="822dc-110">Especifica o nome da conta de automação que contém as configurações de DSC que esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="822dc-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="822dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822dc-111">-DefaultProfile</span></span>
<span data-ttu-id="822dc-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="822dc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="822dc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="822dc-113">-Force</span></span>
<span data-ttu-id="822dc-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="822dc-114">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="822dc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="822dc-115">-Name</span></span>
<span data-ttu-id="822dc-116">Especifica o nome da configuração DSC que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="822dc-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="822dc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="822dc-117">-ResourceGroupName</span></span>
<span data-ttu-id="822dc-118">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém configurações DSC.</span><span class="sxs-lookup"><span data-stu-id="822dc-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="822dc-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="822dc-119">-Confirm</span></span>
<span data-ttu-id="822dc-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="822dc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="822dc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="822dc-121">-WhatIf</span></span>
<span data-ttu-id="822dc-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="822dc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="822dc-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="822dc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="822dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822dc-124">CommonParameters</span></span>
<span data-ttu-id="822dc-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="822dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822dc-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="822dc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822dc-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="822dc-127">INPUTS</span></span>

### <span data-ttu-id="822dc-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="822dc-128">None</span></span>
<span data-ttu-id="822dc-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="822dc-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="822dc-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="822dc-130">OUTPUTS</span></span>

## <span data-ttu-id="822dc-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="822dc-131">NOTES</span></span>

## <span data-ttu-id="822dc-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="822dc-132">RELATED LINKS</span></span>

[<span data-ttu-id="822dc-133">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="822dc-133">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="822dc-134">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="822dc-134">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="822dc-135">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="822dc-135">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


