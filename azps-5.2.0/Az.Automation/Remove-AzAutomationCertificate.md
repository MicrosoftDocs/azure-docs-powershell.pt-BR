---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: e6dd090998d7a61d61fdad4bb40cbe2c62d7df1f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264530"
---
# <span data-ttu-id="191ea-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="191ea-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="191ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="191ea-102">SYNOPSIS</span></span>
<span data-ttu-id="191ea-103">Remove um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="191ea-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="191ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="191ea-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="191ea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="191ea-105">DESCRIPTION</span></span>
<span data-ttu-id="191ea-106">O cmdlet **Remove-AzAutomationCertificate** remove um certificado da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="191ea-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="191ea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="191ea-107">EXAMPLES</span></span>

### <span data-ttu-id="191ea-108">Exemplo 1: remover um certificado</span><span class="sxs-lookup"><span data-stu-id="191ea-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="191ea-109">Esse comando Remove um certificado denominado Cert01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="191ea-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="191ea-110">OS</span><span class="sxs-lookup"><span data-stu-id="191ea-110">PARAMETERS</span></span>

### <span data-ttu-id="191ea-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="191ea-111">-AutomationAccountName</span></span>
<span data-ttu-id="191ea-112">Especifica o nome da conta de automação para a qual esse cmdlet Remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="191ea-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="191ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="191ea-113">-DefaultProfile</span></span>
<span data-ttu-id="191ea-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="191ea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="191ea-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="191ea-115">-Name</span></span>
<span data-ttu-id="191ea-116">Especifica o nome do certificado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="191ea-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="191ea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="191ea-117">-ResourceGroupName</span></span>
<span data-ttu-id="191ea-118">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="191ea-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="191ea-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="191ea-119">-Confirm</span></span>
<span data-ttu-id="191ea-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="191ea-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="191ea-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="191ea-121">-WhatIf</span></span>
<span data-ttu-id="191ea-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="191ea-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="191ea-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="191ea-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="191ea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="191ea-124">CommonParameters</span></span>
<span data-ttu-id="191ea-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="191ea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="191ea-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="191ea-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="191ea-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="191ea-127">INPUTS</span></span>

### <span data-ttu-id="191ea-128">System. String</span><span class="sxs-lookup"><span data-stu-id="191ea-128">System.String</span></span>

## <span data-ttu-id="191ea-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="191ea-129">OUTPUTS</span></span>

### <span data-ttu-id="191ea-130">System. void</span><span class="sxs-lookup"><span data-stu-id="191ea-130">System.Void</span></span>

## <span data-ttu-id="191ea-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="191ea-131">NOTES</span></span>

## <span data-ttu-id="191ea-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="191ea-132">RELATED LINKS</span></span>

[<span data-ttu-id="191ea-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="191ea-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="191ea-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="191ea-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="191ea-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="191ea-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


