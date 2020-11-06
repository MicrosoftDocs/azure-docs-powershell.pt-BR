---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: 7498310c232fd623b131bdf9ae59136d9a4c500a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431439"
---
# <span data-ttu-id="49829-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="49829-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="49829-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49829-102">SYNOPSIS</span></span>
<span data-ttu-id="49829-103">Remove um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="49829-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49829-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49829-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49829-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49829-105">DESCRIPTION</span></span>
<span data-ttu-id="49829-106">O cmdlet **Remove-AzureRmAutomationCertificate** remove um certificado da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="49829-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="49829-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49829-107">EXAMPLES</span></span>

### <span data-ttu-id="49829-108">Exemplo 1: remover um certificado</span><span class="sxs-lookup"><span data-stu-id="49829-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="49829-109">Esse comando Remove um certificado denominado Cert01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="49829-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="49829-110">OS</span><span class="sxs-lookup"><span data-stu-id="49829-110">PARAMETERS</span></span>

### <span data-ttu-id="49829-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="49829-111">-AutomationAccountName</span></span>
<span data-ttu-id="49829-112">Especifica o nome da conta de automação para a qual esse cmdlet Remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="49829-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="49829-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49829-113">-DefaultProfile</span></span>
<span data-ttu-id="49829-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="49829-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49829-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="49829-115">-Name</span></span>
<span data-ttu-id="49829-116">Especifica o nome do certificado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="49829-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="49829-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49829-117">-ResourceGroupName</span></span>
<span data-ttu-id="49829-118">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="49829-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="49829-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="49829-119">-Confirm</span></span>
<span data-ttu-id="49829-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49829-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49829-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49829-121">-WhatIf</span></span>
<span data-ttu-id="49829-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="49829-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49829-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49829-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49829-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49829-124">CommonParameters</span></span>
<span data-ttu-id="49829-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49829-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49829-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49829-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49829-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49829-127">INPUTS</span></span>

### <span data-ttu-id="49829-128">System. String</span><span class="sxs-lookup"><span data-stu-id="49829-128">System.String</span></span>

## <span data-ttu-id="49829-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49829-129">OUTPUTS</span></span>

### <span data-ttu-id="49829-130">System. void</span><span class="sxs-lookup"><span data-stu-id="49829-130">System.Void</span></span>

## <span data-ttu-id="49829-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49829-131">NOTES</span></span>

## <span data-ttu-id="49829-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49829-132">RELATED LINKS</span></span>

[<span data-ttu-id="49829-133">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="49829-133">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="49829-134">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="49829-134">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="49829-135">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="49829-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


