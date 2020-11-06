---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 2cd60a70b057689cf7edf154df28253b86e110a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431169"
---
# <span data-ttu-id="d9e3f-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9e3f-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="d9e3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e3f-103">Remove as configurações DSC da automação.</span><span class="sxs-lookup"><span data-stu-id="d9e3f-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9e3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9e3f-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9e3f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9e3f-105">DESCRIPTION</span></span>
<span data-ttu-id="d9e3f-106">O cmdlet **Remove-AzureRmAutomationDscConfiguration** remove as configurações de estado desejado do APS (DSC) da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9e3f-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="d9e3f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9e3f-107">EXAMPLES</span></span>

## <span data-ttu-id="d9e3f-108">OS</span><span class="sxs-lookup"><span data-stu-id="d9e3f-108">PARAMETERS</span></span>

### <span data-ttu-id="d9e3f-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d9e3f-109">-AutomationAccountName</span></span>
<span data-ttu-id="d9e3f-110">Especifica o nome da conta de automação que contém as configurações de DSC que esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="d9e3f-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d9e3f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d9e3f-111">-Force</span></span>
<span data-ttu-id="d9e3f-112">ps_force</span><span class="sxs-lookup"><span data-stu-id="d9e3f-112">ps_force</span></span>

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

### <span data-ttu-id="d9e3f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9e3f-113">-Name</span></span>
<span data-ttu-id="d9e3f-114">Especifica o nome da configuração DSC que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="d9e3f-114">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d9e3f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9e3f-115">-ResourceGroupName</span></span>
<span data-ttu-id="d9e3f-116">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém configurações DSC.</span><span class="sxs-lookup"><span data-stu-id="d9e3f-116">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="d9e3f-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9e3f-117">-Confirm</span></span>
<span data-ttu-id="d9e3f-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9e3f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9e3f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9e3f-119">-WhatIf</span></span>
<span data-ttu-id="d9e3f-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9e3f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9e3f-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9e3f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9e3f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e3f-122">-DefaultProfile</span></span>
<span data-ttu-id="d9e3f-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9e3f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9e3f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e3f-124">CommonParameters</span></span>
<span data-ttu-id="d9e3f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9e3f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e3f-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9e3f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e3f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9e3f-127">INPUTS</span></span>

## <span data-ttu-id="d9e3f-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9e3f-128">OUTPUTS</span></span>

## <span data-ttu-id="d9e3f-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9e3f-129">NOTES</span></span>

## <span data-ttu-id="d9e3f-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9e3f-130">RELATED LINKS</span></span>

[<span data-ttu-id="d9e3f-131">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9e3f-131">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="d9e3f-132">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9e3f-132">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="d9e3f-133">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9e3f-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


