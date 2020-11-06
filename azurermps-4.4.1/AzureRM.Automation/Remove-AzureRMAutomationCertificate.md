---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: d1230030f95d22d972aa537208b30f350ec9dbe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431821"
---
# <span data-ttu-id="03845-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="03845-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="03845-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03845-102">SYNOPSIS</span></span>
<span data-ttu-id="03845-103">Remove um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="03845-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03845-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03845-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03845-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03845-105">DESCRIPTION</span></span>
<span data-ttu-id="03845-106">O cmdlet **Remove-AzureRmAutomationCertificate** remove um certificado da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="03845-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="03845-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03845-107">EXAMPLES</span></span>

### <span data-ttu-id="03845-108">Exemplo 1: remover um certificado</span><span class="sxs-lookup"><span data-stu-id="03845-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="03845-109">Esse comando Remove um certificado denominado Cert01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="03845-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="03845-110">OS</span><span class="sxs-lookup"><span data-stu-id="03845-110">PARAMETERS</span></span>

### <span data-ttu-id="03845-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="03845-111">-AutomationAccountName</span></span>
<span data-ttu-id="03845-112">Especifica o nome da conta de automação para a qual esse cmdlet Remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="03845-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="03845-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="03845-113">-Name</span></span>
<span data-ttu-id="03845-114">Especifica o nome do certificado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="03845-114">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="03845-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03845-115">-ResourceGroupName</span></span>
<span data-ttu-id="03845-116">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="03845-116">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="03845-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="03845-117">-Confirm</span></span>
<span data-ttu-id="03845-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03845-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03845-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03845-119">-WhatIf</span></span>
<span data-ttu-id="03845-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="03845-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03845-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03845-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03845-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03845-122">-DefaultProfile</span></span>
<span data-ttu-id="03845-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03845-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03845-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03845-124">CommonParameters</span></span>
<span data-ttu-id="03845-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03845-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03845-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03845-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03845-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03845-127">INPUTS</span></span>

## <span data-ttu-id="03845-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03845-128">OUTPUTS</span></span>

## <span data-ttu-id="03845-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03845-129">NOTES</span></span>

## <span data-ttu-id="03845-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03845-130">RELATED LINKS</span></span>

[<span data-ttu-id="03845-131">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="03845-131">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="03845-132">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="03845-132">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="03845-133">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="03845-133">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


