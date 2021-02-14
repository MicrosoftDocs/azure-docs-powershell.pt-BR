---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: d6d233bcd9ac439d163c0b6de6866a0c7dac0b04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116616"
---
# <span data-ttu-id="958be-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="958be-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="958be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="958be-102">SYNOPSIS</span></span>
<span data-ttu-id="958be-103">Remove um nó DSC do gerenciamento por uma conta de Automação.</span><span class="sxs-lookup"><span data-stu-id="958be-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="958be-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="958be-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="958be-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="958be-105">DESCRIPTION</span></span>
<span data-ttu-id="958be-106">O **cmdlet Unregister-AzAutomationDscNode** remove um nó DSC (Configuração de Estado Desejado) APS do gerenciamento por uma conta de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="958be-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="958be-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="958be-107">EXAMPLES</span></span>

### <span data-ttu-id="958be-108">Exemplo 1: Remover um nó DSC do Azure do gerenciamento por uma conta de Automação</span><span class="sxs-lookup"><span data-stu-id="958be-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="958be-109">Esse comando remove o nó DSC que tem o GUID especificado do gerenciamento pela conta de Automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="958be-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="958be-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="958be-110">PARAMETERS</span></span>

### <span data-ttu-id="958be-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="958be-111">-AutomationAccountName</span></span>
<span data-ttu-id="958be-112">Especifica o nome da conta automação da qual este cmdlet remove um nó DSC.</span><span class="sxs-lookup"><span data-stu-id="958be-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="958be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="958be-113">-DefaultProfile</span></span>
<span data-ttu-id="958be-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="958be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="958be-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="958be-115">-Force</span></span>
<span data-ttu-id="958be-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="958be-116">ps_force</span></span>

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

### <span data-ttu-id="958be-117">-ID</span><span class="sxs-lookup"><span data-stu-id="958be-117">-Id</span></span>
<span data-ttu-id="958be-118">Especifica a ID exclusiva do nó DSC que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="958be-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="958be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="958be-119">-ResourceGroupName</span></span>
<span data-ttu-id="958be-120">Especifica o nome de um grupo de recursos no qual este cmdlet não contata um nó DSC.</span><span class="sxs-lookup"><span data-stu-id="958be-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="958be-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="958be-121">-Confirm</span></span>
<span data-ttu-id="958be-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="958be-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="958be-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="958be-123">-WhatIf</span></span>
<span data-ttu-id="958be-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="958be-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="958be-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="958be-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="958be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958be-126">CommonParameters</span></span>
<span data-ttu-id="958be-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="958be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958be-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="958be-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958be-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="958be-129">INPUTS</span></span>

### <span data-ttu-id="958be-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="958be-130">System.Guid</span></span>

### <span data-ttu-id="958be-131">System.String</span><span class="sxs-lookup"><span data-stu-id="958be-131">System.String</span></span>

## <span data-ttu-id="958be-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="958be-132">OUTPUTS</span></span>

### <span data-ttu-id="958be-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="958be-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="958be-134">Notas</span><span class="sxs-lookup"><span data-stu-id="958be-134">NOTES</span></span>

## <span data-ttu-id="958be-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="958be-135">RELATED LINKS</span></span>

[<span data-ttu-id="958be-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="958be-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="958be-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="958be-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="958be-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="958be-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


