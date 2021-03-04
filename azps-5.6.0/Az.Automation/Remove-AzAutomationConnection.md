---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 0534f05bcc59a109851188c8b585badfc90d61c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892898"
---
# <span data-ttu-id="20f84-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="20f84-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="20f84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20f84-102">SYNOPSIS</span></span>
<span data-ttu-id="20f84-103">Remove uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="20f84-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="20f84-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="20f84-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20f84-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="20f84-105">DESCRIPTION</span></span>
<span data-ttu-id="20f84-106">O cmdlet **Remove-AzAutomationConnection** remove uma conexão do Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="20f84-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="20f84-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20f84-107">EXAMPLES</span></span>

### <span data-ttu-id="20f84-108">Exemplo 1: Remover uma conexão</span><span class="sxs-lookup"><span data-stu-id="20f84-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="20f84-109">Este comando remove um certificado chamado ContosoConnection na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="20f84-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="20f84-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="20f84-110">PARAMETERS</span></span>

### <span data-ttu-id="20f84-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="20f84-111">-AutomationAccountName</span></span>
<span data-ttu-id="20f84-112">Especifica o nome da conta de automação para a qual este cmdlet remove uma conexão.</span><span class="sxs-lookup"><span data-stu-id="20f84-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="20f84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f84-113">-DefaultProfile</span></span>
<span data-ttu-id="20f84-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="20f84-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20f84-115">-Force</span><span class="sxs-lookup"><span data-stu-id="20f84-115">-Force</span></span>
<span data-ttu-id="20f84-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="20f84-116">ps_force</span></span>

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

### <span data-ttu-id="20f84-117">-Name</span><span class="sxs-lookup"><span data-stu-id="20f84-117">-Name</span></span>
<span data-ttu-id="20f84-118">Especifica o nome da conexão que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="20f84-118">Specifies the name of the connection that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20f84-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20f84-119">-ResourceGroupName</span></span>
<span data-ttu-id="20f84-120">Especifica o nome do grupo de recursos para o qual este cmdlet remove uma conexão.</span><span class="sxs-lookup"><span data-stu-id="20f84-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="20f84-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20f84-121">-Confirm</span></span>
<span data-ttu-id="20f84-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20f84-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20f84-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20f84-123">-WhatIf</span></span>
<span data-ttu-id="20f84-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20f84-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20f84-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20f84-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20f84-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f84-126">CommonParameters</span></span>
<span data-ttu-id="20f84-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20f84-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f84-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f84-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f84-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20f84-129">INPUTS</span></span>

### <span data-ttu-id="20f84-130">System.String</span><span class="sxs-lookup"><span data-stu-id="20f84-130">System.String</span></span>

## <span data-ttu-id="20f84-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="20f84-131">OUTPUTS</span></span>

### <span data-ttu-id="20f84-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="20f84-132">System.Void</span></span>

## <span data-ttu-id="20f84-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="20f84-133">NOTES</span></span>

## <span data-ttu-id="20f84-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20f84-134">RELATED LINKS</span></span>

[<span data-ttu-id="20f84-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="20f84-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="20f84-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="20f84-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


