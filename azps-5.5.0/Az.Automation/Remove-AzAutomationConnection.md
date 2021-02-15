---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118014"
---
# <span data-ttu-id="710bb-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="710bb-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="710bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="710bb-102">SYNOPSIS</span></span>
<span data-ttu-id="710bb-103">Remove uma conexão automação.</span><span class="sxs-lookup"><span data-stu-id="710bb-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="710bb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="710bb-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="710bb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="710bb-105">DESCRIPTION</span></span>
<span data-ttu-id="710bb-106">O cmdlet **Remove-AzAutomationConnection** remove uma conexão da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="710bb-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="710bb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="710bb-107">EXAMPLES</span></span>

### <span data-ttu-id="710bb-108">Exemplo 1: Remover uma conexão</span><span class="sxs-lookup"><span data-stu-id="710bb-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="710bb-109">Esse comando remove um certificado chamado ContosoConnection na conta de Automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="710bb-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="710bb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="710bb-110">PARAMETERS</span></span>

### <span data-ttu-id="710bb-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="710bb-111">-AutomationAccountName</span></span>
<span data-ttu-id="710bb-112">Especifica o nome da conta de automação para a qual este cmdlet remove uma conexão.</span><span class="sxs-lookup"><span data-stu-id="710bb-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="710bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="710bb-113">-DefaultProfile</span></span>
<span data-ttu-id="710bb-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="710bb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="710bb-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="710bb-115">-Force</span></span>
<span data-ttu-id="710bb-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="710bb-116">ps_force</span></span>

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

### <span data-ttu-id="710bb-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="710bb-117">-Name</span></span>
<span data-ttu-id="710bb-118">Especifica o nome da conexão que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="710bb-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="710bb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="710bb-119">-ResourceGroupName</span></span>
<span data-ttu-id="710bb-120">Especifica o nome do grupo de recursos para o qual este cmdlet remove uma conexão.</span><span class="sxs-lookup"><span data-stu-id="710bb-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="710bb-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="710bb-121">-Confirm</span></span>
<span data-ttu-id="710bb-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="710bb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="710bb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="710bb-123">-WhatIf</span></span>
<span data-ttu-id="710bb-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="710bb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="710bb-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="710bb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="710bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="710bb-126">CommonParameters</span></span>
<span data-ttu-id="710bb-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="710bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="710bb-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="710bb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="710bb-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="710bb-129">INPUTS</span></span>

### <span data-ttu-id="710bb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="710bb-130">System.String</span></span>

## <span data-ttu-id="710bb-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="710bb-131">OUTPUTS</span></span>

### <span data-ttu-id="710bb-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="710bb-132">System.Void</span></span>

## <span data-ttu-id="710bb-133">Notas</span><span class="sxs-lookup"><span data-stu-id="710bb-133">NOTES</span></span>

## <span data-ttu-id="710bb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="710bb-134">RELATED LINKS</span></span>

[<span data-ttu-id="710bb-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="710bb-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="710bb-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="710bb-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


