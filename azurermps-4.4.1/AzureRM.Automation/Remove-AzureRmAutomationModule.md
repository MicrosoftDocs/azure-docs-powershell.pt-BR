---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 42fc322e9f593ecad6c295952d46274eb2563799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431166"
---
# <span data-ttu-id="61e06-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="61e06-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="61e06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61e06-102">SYNOPSIS</span></span>
<span data-ttu-id="61e06-103">Remove um módulo da automação.</span><span class="sxs-lookup"><span data-stu-id="61e06-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61e06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61e06-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61e06-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61e06-105">DESCRIPTION</span></span>
<span data-ttu-id="61e06-106">O cmdlet **Remove-AzureRmAutomationModule** remove um módulo de uma conta de automação na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="61e06-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="61e06-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61e06-107">EXAMPLES</span></span>

### <span data-ttu-id="61e06-108">Exemplo 1: remover um módulo</span><span class="sxs-lookup"><span data-stu-id="61e06-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="61e06-109">Esse comando Remove um módulo chamado ContosoModule da conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="61e06-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="61e06-110">OS</span><span class="sxs-lookup"><span data-stu-id="61e06-110">PARAMETERS</span></span>

### <span data-ttu-id="61e06-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="61e06-111">-AutomationAccountName</span></span>
<span data-ttu-id="61e06-112">Especifica o nome da conta de automação a partir da qual esse cmdlet Remove um módulo.</span><span class="sxs-lookup"><span data-stu-id="61e06-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="61e06-113">-Force</span><span class="sxs-lookup"><span data-stu-id="61e06-113">-Force</span></span>
<span data-ttu-id="61e06-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="61e06-114">ps_force</span></span>

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

### <span data-ttu-id="61e06-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="61e06-115">-Name</span></span>
<span data-ttu-id="61e06-116">Especifica o nome do módulo que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="61e06-116">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="61e06-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61e06-117">-ResourceGroupName</span></span>
<span data-ttu-id="61e06-118">Especifica o nome de um grupo de recursos em que esse cmdlet Remove um módulo.</span><span class="sxs-lookup"><span data-stu-id="61e06-118">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="61e06-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="61e06-119">-Confirm</span></span>
<span data-ttu-id="61e06-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61e06-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61e06-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e06-121">-WhatIf</span></span>
<span data-ttu-id="61e06-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="61e06-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61e06-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="61e06-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61e06-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e06-124">-DefaultProfile</span></span>
<span data-ttu-id="61e06-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61e06-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61e06-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e06-126">CommonParameters</span></span>
<span data-ttu-id="61e06-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e06-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e06-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61e06-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e06-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61e06-129">INPUTS</span></span>

## <span data-ttu-id="61e06-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61e06-130">OUTPUTS</span></span>

## <span data-ttu-id="61e06-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61e06-131">NOTES</span></span>

## <span data-ttu-id="61e06-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61e06-132">RELATED LINKS</span></span>

[<span data-ttu-id="61e06-133">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="61e06-133">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="61e06-134">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="61e06-134">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="61e06-135">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="61e06-135">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


