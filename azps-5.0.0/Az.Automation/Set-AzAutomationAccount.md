---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: f32e9c0d76e88fba5475abb39595b0a6c4bea834
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282084"
---
# <span data-ttu-id="06226-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="06226-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="06226-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06226-102">SYNOPSIS</span></span>
<span data-ttu-id="06226-103">Modifica uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="06226-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="06226-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06226-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06226-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06226-105">DESCRIPTION</span></span>
<span data-ttu-id="06226-106">O cmdlet **set-AzAutomationAccount** modifica uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="06226-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="06226-107">Para obter mais informações sobre contas de automação, consulte o cmdlet New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="06226-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="06226-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06226-108">EXAMPLES</span></span>

### <span data-ttu-id="06226-109">Exemplo 1: definir as marcas para uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="06226-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="06226-110">O primeiro comando atribui dois pares de chave/valor à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="06226-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="06226-111">O segundo comando define marcas em $Tags para a conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="06226-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="06226-112">Exemplo 2: alterar o plano para uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="06226-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="06226-113">Esse comando altera o plano para Basic para a conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="06226-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="06226-114">OS</span><span class="sxs-lookup"><span data-stu-id="06226-114">PARAMETERS</span></span>

### <span data-ttu-id="06226-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06226-115">-DefaultProfile</span></span>
<span data-ttu-id="06226-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="06226-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06226-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="06226-117">-Name</span></span>
<span data-ttu-id="06226-118">Especifica o nome da conta de automação modificada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06226-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06226-119">-Plano</span><span class="sxs-lookup"><span data-stu-id="06226-119">-Plan</span></span>
<span data-ttu-id="06226-120">Especifica o plano para a conta de automação.</span><span class="sxs-lookup"><span data-stu-id="06226-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="06226-121">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="06226-121">Valid values are:</span></span>
- <span data-ttu-id="06226-122">Basic</span><span class="sxs-lookup"><span data-stu-id="06226-122">Basic</span></span>
- <span data-ttu-id="06226-123">Gratuito</span><span class="sxs-lookup"><span data-stu-id="06226-123">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06226-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06226-124">-ResourceGroupName</span></span>
<span data-ttu-id="06226-125">Especifica o nome de um grupo de recursos que contém a conta de automação que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="06226-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="06226-126">-Marcas</span><span class="sxs-lookup"><span data-stu-id="06226-126">-Tags</span></span>
<span data-ttu-id="06226-127">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="06226-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="06226-128">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="06226-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06226-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06226-129">CommonParameters</span></span>
<span data-ttu-id="06226-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06226-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06226-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06226-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06226-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06226-132">INPUTS</span></span>

### <span data-ttu-id="06226-133">System. String</span><span class="sxs-lookup"><span data-stu-id="06226-133">System.String</span></span>

### <span data-ttu-id="06226-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="06226-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="06226-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06226-135">OUTPUTS</span></span>

### <span data-ttu-id="06226-136">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="06226-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="06226-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06226-137">NOTES</span></span>

## <span data-ttu-id="06226-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06226-138">RELATED LINKS</span></span>

[<span data-ttu-id="06226-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="06226-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="06226-140">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="06226-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="06226-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="06226-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
