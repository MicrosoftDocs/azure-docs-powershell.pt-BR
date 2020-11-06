---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 60f80f92723bbb66d1bf88c9fd8efea66c8c4e55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428624"
---
# <span data-ttu-id="ca2c4-101">Remove-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca2c4-101">Remove-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="ca2c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca2c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ca2c4-103">Remove metadados das configurações do nó DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="ca2c4-103">Removes metadata from DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca2c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca2c4-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca2c4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca2c4-105">DESCRIPTION</span></span>
<span data-ttu-id="ca2c4-106">O cmdlet **Remove-AzureRmAutomationDscNodeConfiguration** remove metadados das configurações do nó DSC (configuração de estado desejado do APS) na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca2c4-106">The **Remove-AzureRmAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="ca2c4-107">A automação armazena a configuração do nó DSC como um documento de configuração do MOF (formato de objeto gerenciado).</span><span class="sxs-lookup"><span data-stu-id="ca2c4-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="ca2c4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca2c4-108">EXAMPLES</span></span>

## <span data-ttu-id="ca2c4-109">OS</span><span class="sxs-lookup"><span data-stu-id="ca2c4-109">PARAMETERS</span></span>

### <span data-ttu-id="ca2c4-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ca2c4-110">-AutomationAccountName</span></span>
<span data-ttu-id="ca2c4-111">Especifica o nome de uma conta de automação que contém as configurações de nó DSC para as quais esse cmdlet Remove metadados.</span><span class="sxs-lookup"><span data-stu-id="ca2c4-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="ca2c4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca2c4-112">-DefaultProfile</span></span>
<span data-ttu-id="ca2c4-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ca2c4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca2c4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ca2c4-114">-Force</span></span>
<span data-ttu-id="ca2c4-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="ca2c4-115">ps_force</span></span>

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

### <span data-ttu-id="ca2c4-116">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="ca2c4-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="ca2c4-117">Indica que esse cmdlet ignora mapeamentos de nó.</span><span class="sxs-lookup"><span data-stu-id="ca2c4-117">Indicates that this cmdlet ignores node mappings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca2c4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca2c4-118">-Name</span></span>
<span data-ttu-id="ca2c4-119">Especifica o nome da configuração do nó DSC para a qual esse cmdlet Remove metadados.</span><span class="sxs-lookup"><span data-stu-id="ca2c4-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca2c4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca2c4-120">-ResourceGroupName</span></span>
<span data-ttu-id="ca2c4-121">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca2c4-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ca2c4-122">Esse cmdlet Remove metadados de configurações de nó DSC no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ca2c4-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ca2c4-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca2c4-123">-Confirm</span></span>
<span data-ttu-id="ca2c4-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca2c4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca2c4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca2c4-125">-WhatIf</span></span>
<span data-ttu-id="ca2c4-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca2c4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca2c4-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca2c4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca2c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca2c4-128">CommonParameters</span></span>
<span data-ttu-id="ca2c4-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca2c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca2c4-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca2c4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca2c4-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca2c4-131">INPUTS</span></span>

### <span data-ttu-id="ca2c4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ca2c4-132">System.String</span></span>

## <span data-ttu-id="ca2c4-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca2c4-133">OUTPUTS</span></span>

### <span data-ttu-id="ca2c4-134">System. void</span><span class="sxs-lookup"><span data-stu-id="ca2c4-134">System.Void</span></span>

## <span data-ttu-id="ca2c4-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca2c4-135">NOTES</span></span>

## <span data-ttu-id="ca2c4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca2c4-136">RELATED LINKS</span></span>

[<span data-ttu-id="ca2c4-137">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca2c4-137">Get-AzureRmAutomationDscNodeConfiguration</span></span>](./Get-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="ca2c4-138">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca2c4-138">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="ca2c4-139">Cmdlets de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="ca2c4-139">Azure Automation Cmdlets</span></span>](./AzureRM.Automation.md)


