---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 2c98cde73610a7a72b237bbe268f527fefaf71a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431818"
---
# <span data-ttu-id="e05ad-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e05ad-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="e05ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e05ad-102">SYNOPSIS</span></span>
<span data-ttu-id="e05ad-103">Remove uma credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="e05ad-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e05ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e05ad-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e05ad-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e05ad-105">DESCRIPTION</span></span>
<span data-ttu-id="e05ad-106">O cmdlet **Remove-AzureRmAutomationCredential** remove uma credencial da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="e05ad-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="e05ad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e05ad-107">EXAMPLES</span></span>

### <span data-ttu-id="e05ad-108">Exemplo 1: remover uma credencial</span><span class="sxs-lookup"><span data-stu-id="e05ad-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e05ad-109">Esse comando Remove uma credencial chamada ContosoCredential na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e05ad-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e05ad-110">OS</span><span class="sxs-lookup"><span data-stu-id="e05ad-110">PARAMETERS</span></span>

### <span data-ttu-id="e05ad-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e05ad-111">-AutomationAccountName</span></span>
<span data-ttu-id="e05ad-112">Especifica o nome da conta de automação a partir da qual esse cmdlet Remove uma credencial.</span><span class="sxs-lookup"><span data-stu-id="e05ad-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="e05ad-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e05ad-113">-Name</span></span>
<span data-ttu-id="e05ad-114">Especifica o nome da credencial que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e05ad-114">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e05ad-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e05ad-115">-ResourceGroupName</span></span>
<span data-ttu-id="e05ad-116">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove uma credencial.</span><span class="sxs-lookup"><span data-stu-id="e05ad-116">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="e05ad-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e05ad-117">-Confirm</span></span>
<span data-ttu-id="e05ad-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e05ad-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e05ad-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e05ad-119">-WhatIf</span></span>
<span data-ttu-id="e05ad-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e05ad-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e05ad-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e05ad-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e05ad-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05ad-122">-DefaultProfile</span></span>
<span data-ttu-id="e05ad-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e05ad-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e05ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05ad-124">CommonParameters</span></span>
<span data-ttu-id="e05ad-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05ad-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e05ad-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05ad-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e05ad-127">INPUTS</span></span>

## <span data-ttu-id="e05ad-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e05ad-128">OUTPUTS</span></span>

## <span data-ttu-id="e05ad-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e05ad-129">NOTES</span></span>

## <span data-ttu-id="e05ad-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e05ad-130">RELATED LINKS</span></span>

[<span data-ttu-id="e05ad-131">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e05ad-131">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="e05ad-132">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e05ad-132">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="e05ad-133">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e05ad-133">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


