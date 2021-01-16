---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264531"
---
# <span data-ttu-id="10da6-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="10da6-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="10da6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10da6-102">SYNOPSIS</span></span>
<span data-ttu-id="10da6-103">Remove uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="10da6-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="10da6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10da6-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10da6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10da6-105">DESCRIPTION</span></span>
<span data-ttu-id="10da6-106">O cmdlet **Remove-AzAutomationConnection** remove uma conexão da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="10da6-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="10da6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10da6-107">EXAMPLES</span></span>

### <span data-ttu-id="10da6-108">Exemplo 1: remover uma conexão</span><span class="sxs-lookup"><span data-stu-id="10da6-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="10da6-109">Esse comando Remove um certificado denominado ContosoConnection na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="10da6-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="10da6-110">OS</span><span class="sxs-lookup"><span data-stu-id="10da6-110">PARAMETERS</span></span>

### <span data-ttu-id="10da6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="10da6-111">-AutomationAccountName</span></span>
<span data-ttu-id="10da6-112">Especifica o nome da conta de automação para a qual esse cmdlet Remove uma conexão.</span><span class="sxs-lookup"><span data-stu-id="10da6-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="10da6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10da6-113">-DefaultProfile</span></span>
<span data-ttu-id="10da6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="10da6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10da6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="10da6-115">-Force</span></span>
<span data-ttu-id="10da6-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="10da6-116">ps_force</span></span>

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

### <span data-ttu-id="10da6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="10da6-117">-Name</span></span>
<span data-ttu-id="10da6-118">Especifica o nome da conexão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="10da6-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="10da6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10da6-119">-ResourceGroupName</span></span>
<span data-ttu-id="10da6-120">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove uma conexão.</span><span class="sxs-lookup"><span data-stu-id="10da6-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="10da6-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="10da6-121">-Confirm</span></span>
<span data-ttu-id="10da6-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10da6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10da6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10da6-123">-WhatIf</span></span>
<span data-ttu-id="10da6-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10da6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10da6-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10da6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10da6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10da6-126">CommonParameters</span></span>
<span data-ttu-id="10da6-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10da6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10da6-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10da6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10da6-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10da6-129">INPUTS</span></span>

### <span data-ttu-id="10da6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="10da6-130">System.String</span></span>

## <span data-ttu-id="10da6-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10da6-131">OUTPUTS</span></span>

### <span data-ttu-id="10da6-132">System. void</span><span class="sxs-lookup"><span data-stu-id="10da6-132">System.Void</span></span>

## <span data-ttu-id="10da6-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10da6-133">NOTES</span></span>

## <span data-ttu-id="10da6-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10da6-134">RELATED LINKS</span></span>

[<span data-ttu-id="10da6-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="10da6-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="10da6-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="10da6-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


