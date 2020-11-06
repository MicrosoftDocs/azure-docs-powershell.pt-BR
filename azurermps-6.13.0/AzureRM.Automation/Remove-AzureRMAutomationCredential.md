---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 6c0fe1185bfa8d5233371788da87e7a13fe32c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427309"
---
# <span data-ttu-id="03088-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="03088-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="03088-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03088-102">SYNOPSIS</span></span>
<span data-ttu-id="03088-103">Remove uma credencial de automação.</span><span class="sxs-lookup"><span data-stu-id="03088-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03088-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03088-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03088-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03088-105">DESCRIPTION</span></span>
<span data-ttu-id="03088-106">O cmdlet **Remove-AzureRmAutomationCredential** remove uma credencial da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="03088-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="03088-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03088-107">EXAMPLES</span></span>

### <span data-ttu-id="03088-108">Exemplo 1: remover uma credencial</span><span class="sxs-lookup"><span data-stu-id="03088-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="03088-109">Esse comando Remove uma credencial chamada ContosoCredential na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="03088-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="03088-110">OS</span><span class="sxs-lookup"><span data-stu-id="03088-110">PARAMETERS</span></span>

### <span data-ttu-id="03088-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="03088-111">-AutomationAccountName</span></span>
<span data-ttu-id="03088-112">Especifica o nome da conta de automação a partir da qual esse cmdlet Remove uma credencial.</span><span class="sxs-lookup"><span data-stu-id="03088-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="03088-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03088-113">-DefaultProfile</span></span>
<span data-ttu-id="03088-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="03088-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03088-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="03088-115">-Name</span></span>
<span data-ttu-id="03088-116">Especifica o nome da credencial que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="03088-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="03088-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03088-117">-ResourceGroupName</span></span>
<span data-ttu-id="03088-118">Especifica o nome do grupo de recursos para o qual esse cmdlet Remove uma credencial.</span><span class="sxs-lookup"><span data-stu-id="03088-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="03088-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="03088-119">-Confirm</span></span>
<span data-ttu-id="03088-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03088-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03088-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03088-121">-WhatIf</span></span>
<span data-ttu-id="03088-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="03088-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03088-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03088-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03088-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03088-124">CommonParameters</span></span>
<span data-ttu-id="03088-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03088-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03088-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03088-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03088-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03088-127">INPUTS</span></span>

### <span data-ttu-id="03088-128">System. String</span><span class="sxs-lookup"><span data-stu-id="03088-128">System.String</span></span>

## <span data-ttu-id="03088-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03088-129">OUTPUTS</span></span>

### <span data-ttu-id="03088-130">System. void</span><span class="sxs-lookup"><span data-stu-id="03088-130">System.Void</span></span>

## <span data-ttu-id="03088-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03088-131">NOTES</span></span>

## <span data-ttu-id="03088-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03088-132">RELATED LINKS</span></span>

[<span data-ttu-id="03088-133">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="03088-133">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="03088-134">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="03088-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="03088-135">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="03088-135">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


