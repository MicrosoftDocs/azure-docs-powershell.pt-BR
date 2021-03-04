---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: 5c8d58024f14e2dbd1be929ddb6f156b479d2487
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890307"
---
# <span data-ttu-id="37dd7-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="37dd7-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="37dd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="37dd7-103">Remove um nó DSC do gerenciamento por uma conta de Automação.</span><span class="sxs-lookup"><span data-stu-id="37dd7-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="37dd7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="37dd7-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37dd7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="37dd7-105">DESCRIPTION</span></span>
<span data-ttu-id="37dd7-106">O cmdlet **Unregister-AzAutomationDscNode** remove um nó DSC (Configuração de Estado Desejado) do APS do gerenciamento por uma conta de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="37dd7-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="37dd7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37dd7-107">EXAMPLES</span></span>

### <span data-ttu-id="37dd7-108">Exemplo 1: Remover um nó DSC do Azure do gerenciamento por uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="37dd7-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="37dd7-109">Este comando remove o nó DSC que tem o GUID especificado do gerenciamento pela conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="37dd7-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="37dd7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="37dd7-110">PARAMETERS</span></span>

### <span data-ttu-id="37dd7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="37dd7-111">-AutomationAccountName</span></span>
<span data-ttu-id="37dd7-112">Especifica o nome da conta automação da qual esse cmdlet remove um nó DSC.</span><span class="sxs-lookup"><span data-stu-id="37dd7-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="37dd7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37dd7-113">-DefaultProfile</span></span>
<span data-ttu-id="37dd7-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="37dd7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37dd7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="37dd7-115">-Force</span></span>
<span data-ttu-id="37dd7-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="37dd7-116">ps_force</span></span>

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

### <span data-ttu-id="37dd7-117">-Id</span><span class="sxs-lookup"><span data-stu-id="37dd7-117">-Id</span></span>
<span data-ttu-id="37dd7-118">Especifica a ID exclusiva do nó DSC que esse cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="37dd7-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37dd7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37dd7-119">-ResourceGroupName</span></span>
<span data-ttu-id="37dd7-120">Especifica o nome de um grupo de recursos no qual esse cmdlet não registrou um nó DSC.</span><span class="sxs-lookup"><span data-stu-id="37dd7-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="37dd7-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37dd7-121">-Confirm</span></span>
<span data-ttu-id="37dd7-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37dd7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37dd7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37dd7-123">-WhatIf</span></span>
<span data-ttu-id="37dd7-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37dd7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37dd7-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37dd7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37dd7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37dd7-126">CommonParameters</span></span>
<span data-ttu-id="37dd7-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37dd7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37dd7-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37dd7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37dd7-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37dd7-129">INPUTS</span></span>

### <span data-ttu-id="37dd7-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="37dd7-130">System.Guid</span></span>

### <span data-ttu-id="37dd7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="37dd7-131">System.String</span></span>

## <span data-ttu-id="37dd7-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="37dd7-132">OUTPUTS</span></span>

### <span data-ttu-id="37dd7-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="37dd7-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="37dd7-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="37dd7-134">NOTES</span></span>

## <span data-ttu-id="37dd7-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37dd7-135">RELATED LINKS</span></span>

[<span data-ttu-id="37dd7-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="37dd7-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="37dd7-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="37dd7-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="37dd7-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="37dd7-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


