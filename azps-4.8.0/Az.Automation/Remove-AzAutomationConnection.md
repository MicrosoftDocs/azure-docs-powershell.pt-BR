---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954458"
---
# <span data-ttu-id="a6762-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a6762-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="a6762-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6762-102">SYNOPSIS</span></span>
<span data-ttu-id="a6762-103">Remove uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="a6762-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="a6762-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6762-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6762-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6762-105">DESCRIPTION</span></span>
<span data-ttu-id="a6762-106">O cmdlet **Remove-AzAutomationConnection** remove uma conexão da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6762-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="a6762-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6762-107">EXAMPLES</span></span>

### <span data-ttu-id="a6762-108">Exemplo 1: remover uma conexão</span><span class="sxs-lookup"><span data-stu-id="a6762-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a6762-109">Esse comando Remove um certificado denominado ContosoConnection na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a6762-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a6762-110">OS</span><span class="sxs-lookup"><span data-stu-id="a6762-110">PARAMETERS</span></span>

### <span data-ttu-id="a6762-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a6762-111">-AutomationAccountName</span></span>
<span data-ttu-id="a6762-112">Especifica o nome da conta de automação para a qual esse cmdlet Remove uma conexão.</span><span class="sxs-lookup"><span data-stu-id="a6762-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="a6762-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6762-113">-DefaultProfile</span></span>
<span data-ttu-id="a6762-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a6762-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6762-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a6762-115">-Force</span></span>
<span data-ttu-id="a6762-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="a6762-116">ps_force</span></span>

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

### <span data-ttu-id="a6762-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6762-117">-Name</span></span>
<span data-ttu-id="a6762-118">Especifica o nome da conexão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="a6762-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a6762-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6762-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6762-120">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove uma conexão.</span><span class="sxs-lookup"><span data-stu-id="a6762-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="a6762-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6762-121">-Confirm</span></span>
<span data-ttu-id="a6762-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6762-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6762-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6762-123">-WhatIf</span></span>
<span data-ttu-id="a6762-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6762-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6762-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6762-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6762-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6762-126">CommonParameters</span></span>
<span data-ttu-id="a6762-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6762-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6762-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6762-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6762-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6762-129">INPUTS</span></span>

### <span data-ttu-id="a6762-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a6762-130">System.String</span></span>

## <span data-ttu-id="a6762-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6762-131">OUTPUTS</span></span>

### <span data-ttu-id="a6762-132">System. void</span><span class="sxs-lookup"><span data-stu-id="a6762-132">System.Void</span></span>

## <span data-ttu-id="a6762-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6762-133">NOTES</span></span>

## <span data-ttu-id="a6762-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6762-134">RELATED LINKS</span></span>

[<span data-ttu-id="a6762-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a6762-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="a6762-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a6762-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


