---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: e6dd090998d7a61d61fdad4bb40cbe2c62d7df1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118016"
---
# <span data-ttu-id="41cd6-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="41cd6-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="41cd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="41cd6-103">Remove um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="41cd6-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="41cd6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41cd6-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41cd6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="41cd6-105">DESCRIPTION</span></span>
<span data-ttu-id="41cd6-106">O cmdlet **Remove-AzAutomationCertificate** remove um certificado da Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="41cd6-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="41cd6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="41cd6-107">EXAMPLES</span></span>

### <span data-ttu-id="41cd6-108">Exemplo 1: Remover um certificado</span><span class="sxs-lookup"><span data-stu-id="41cd6-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="41cd6-109">Esse comando remove um certificado chamado Cert01 na conta automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="41cd6-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="41cd6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41cd6-110">PARAMETERS</span></span>

### <span data-ttu-id="41cd6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="41cd6-111">-AutomationAccountName</span></span>
<span data-ttu-id="41cd6-112">Especifica o nome da conta automação para a qual este cmdlet remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="41cd6-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="41cd6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41cd6-113">-DefaultProfile</span></span>
<span data-ttu-id="41cd6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="41cd6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41cd6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="41cd6-115">-Name</span></span>
<span data-ttu-id="41cd6-116">Especifica o nome do certificado que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="41cd6-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="41cd6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41cd6-117">-ResourceGroupName</span></span>
<span data-ttu-id="41cd6-118">Especifica o nome do grupo de recursos para o qual este cmdlet remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="41cd6-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="41cd6-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="41cd6-119">-Confirm</span></span>
<span data-ttu-id="41cd6-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41cd6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41cd6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41cd6-121">-WhatIf</span></span>
<span data-ttu-id="41cd6-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="41cd6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41cd6-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41cd6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41cd6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41cd6-124">CommonParameters</span></span>
<span data-ttu-id="41cd6-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41cd6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41cd6-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41cd6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41cd6-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="41cd6-127">INPUTS</span></span>

### <span data-ttu-id="41cd6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="41cd6-128">System.String</span></span>

## <span data-ttu-id="41cd6-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="41cd6-129">OUTPUTS</span></span>

### <span data-ttu-id="41cd6-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="41cd6-130">System.Void</span></span>

## <span data-ttu-id="41cd6-131">Notas</span><span class="sxs-lookup"><span data-stu-id="41cd6-131">NOTES</span></span>

## <span data-ttu-id="41cd6-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41cd6-132">RELATED LINKS</span></span>

[<span data-ttu-id="41cd6-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="41cd6-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="41cd6-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="41cd6-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="41cd6-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="41cd6-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


