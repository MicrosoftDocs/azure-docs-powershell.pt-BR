---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
ms.openlocfilehash: 1a556a92d59830a4be331c8415fde0c85ddba539
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597763"
---
# <span data-ttu-id="1dbce-101">Remove-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dbce-101">Remove-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="1dbce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1dbce-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbce-103">Remove as configurações DSC da automação.</span><span class="sxs-lookup"><span data-stu-id="1dbce-103">Removes DSC configurations from Automation.</span></span>

## <span data-ttu-id="1dbce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dbce-104">SYNTAX</span></span>

```
Remove-AzAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dbce-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1dbce-105">DESCRIPTION</span></span>
<span data-ttu-id="1dbce-106">O cmdlet **Remove-AzAutomationDscConfiguration** remove as configurações de estado desejado do APS (DSC) da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="1dbce-106">The **Remove-AzAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="1dbce-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1dbce-107">EXAMPLES</span></span>

## <span data-ttu-id="1dbce-108">OS</span><span class="sxs-lookup"><span data-stu-id="1dbce-108">PARAMETERS</span></span>

### <span data-ttu-id="1dbce-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1dbce-109">-AutomationAccountName</span></span>
<span data-ttu-id="1dbce-110">Especifica o nome da conta de automação que contém as configurações de DSC que esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="1dbce-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1dbce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbce-111">-DefaultProfile</span></span>
<span data-ttu-id="1dbce-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1dbce-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dbce-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1dbce-113">-Force</span></span>
<span data-ttu-id="1dbce-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="1dbce-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbce-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dbce-115">-Name</span></span>
<span data-ttu-id="1dbce-116">Especifica o nome da configuração DSC que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="1dbce-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbce-117">-ResourceGroupName</span></span>
<span data-ttu-id="1dbce-118">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém configurações DSC.</span><span class="sxs-lookup"><span data-stu-id="1dbce-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="1dbce-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1dbce-119">-Confirm</span></span>
<span data-ttu-id="1dbce-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dbce-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dbce-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dbce-121">-WhatIf</span></span>
<span data-ttu-id="1dbce-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1dbce-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dbce-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1dbce-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dbce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbce-124">CommonParameters</span></span>
<span data-ttu-id="1dbce-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbce-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dbce-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbce-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1dbce-127">INPUTS</span></span>

### <span data-ttu-id="1dbce-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1dbce-128">System.String</span></span>

## <span data-ttu-id="1dbce-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1dbce-129">OUTPUTS</span></span>

### <span data-ttu-id="1dbce-130">System. void</span><span class="sxs-lookup"><span data-stu-id="1dbce-130">System.Void</span></span>

## <span data-ttu-id="1dbce-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1dbce-131">NOTES</span></span>

## <span data-ttu-id="1dbce-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1dbce-132">RELATED LINKS</span></span>

[<span data-ttu-id="1dbce-133">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dbce-133">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="1dbce-134">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dbce-134">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="1dbce-135">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dbce-135">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


