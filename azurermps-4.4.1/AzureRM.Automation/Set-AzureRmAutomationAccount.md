---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: 8ad63c37c366c0f9c7693585f3a3c2fd57de4fdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428300"
---
# <span data-ttu-id="093fc-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="093fc-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="093fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="093fc-102">SYNOPSIS</span></span>
<span data-ttu-id="093fc-103">Modifica uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="093fc-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="093fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="093fc-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="093fc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="093fc-105">DESCRIPTION</span></span>
<span data-ttu-id="093fc-106">O cmdlet **set-AzureRmAutomationAccount** modifica uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="093fc-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>

<span data-ttu-id="093fc-107">Para obter mais informações sobre contas de automação, consulte o cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="093fc-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="093fc-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="093fc-108">EXAMPLES</span></span>

### <span data-ttu-id="093fc-109">Exemplo 1: definir as marcas para uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="093fc-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="093fc-110">O primeiro comando atribui dois pares de chave/valor à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="093fc-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="093fc-111">O segundo comando define marcas em $Tags para a conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="093fc-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="093fc-112">Exemplo 2: alterar o plano para uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="093fc-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="093fc-113">Esse comando altera o plano para Basic para a conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="093fc-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="093fc-114">OS</span><span class="sxs-lookup"><span data-stu-id="093fc-114">PARAMETERS</span></span>

### <span data-ttu-id="093fc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="093fc-115">-Name</span></span>
<span data-ttu-id="093fc-116">Especifica o nome da conta de automação modificada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="093fc-116">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="093fc-117">-Plano</span><span class="sxs-lookup"><span data-stu-id="093fc-117">-Plan</span></span>
<span data-ttu-id="093fc-118">Especifica o plano para a conta de automação.</span><span class="sxs-lookup"><span data-stu-id="093fc-118">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="093fc-119">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="093fc-119">Valid values are:</span></span>

- <span data-ttu-id="093fc-120">Basic</span><span class="sxs-lookup"><span data-stu-id="093fc-120">Basic</span></span>
- <span data-ttu-id="093fc-121">Gratuito</span><span class="sxs-lookup"><span data-stu-id="093fc-121">Free</span></span>

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

### <span data-ttu-id="093fc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="093fc-122">-ResourceGroupName</span></span>
<span data-ttu-id="093fc-123">Especifica o nome de um grupo de recursos que contém a conta de automação que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="093fc-123">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="093fc-124">-Marcas</span><span class="sxs-lookup"><span data-stu-id="093fc-124">-Tags</span></span>
<span data-ttu-id="093fc-125">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="093fc-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="093fc-126">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="093fc-126">For example:</span></span>

<span data-ttu-id="093fc-127">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="093fc-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="093fc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="093fc-128">-DefaultProfile</span></span>
<span data-ttu-id="093fc-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="093fc-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="093fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="093fc-130">CommonParameters</span></span>
<span data-ttu-id="093fc-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="093fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="093fc-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="093fc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="093fc-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="093fc-133">INPUTS</span></span>

## <span data-ttu-id="093fc-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="093fc-134">OUTPUTS</span></span>

### <span data-ttu-id="093fc-135">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="093fc-135">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="093fc-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="093fc-136">NOTES</span></span>

## <span data-ttu-id="093fc-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="093fc-137">RELATED LINKS</span></span>

[<span data-ttu-id="093fc-138">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="093fc-138">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="093fc-139">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="093fc-139">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="093fc-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="093fc-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
