---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942718"
---
# <span data-ttu-id="60717-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="60717-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="60717-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60717-102">SYNOPSIS</span></span>
<span data-ttu-id="60717-103">Obtém contas de automação em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60717-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="60717-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60717-104">SYNTAX</span></span>

### <span data-ttu-id="60717-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="60717-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60717-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="60717-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60717-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60717-107">DESCRIPTION</span></span>
<span data-ttu-id="60717-108">O cmdlet **Get-AzAutomationAccount** Obtém contas de automação do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60717-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="60717-109">Para obter mais informações sobre contas de automação, consulte o cmdlet New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="60717-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="60717-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60717-110">EXAMPLES</span></span>

### <span data-ttu-id="60717-111">Exemplo 1: obter todas as contas</span><span class="sxs-lookup"><span data-stu-id="60717-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="60717-112">Esse comando obtém todas as contas de automação no grupo de recursos chamado ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="60717-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="60717-113">Exemplo 2: obter uma conta</span><span class="sxs-lookup"><span data-stu-id="60717-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="60717-114">Esse comando obtém a conta de automação chamada ContosoAutomationAccount no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="60717-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="60717-115">OS</span><span class="sxs-lookup"><span data-stu-id="60717-115">PARAMETERS</span></span>

### <span data-ttu-id="60717-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60717-116">-DefaultProfile</span></span>
<span data-ttu-id="60717-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="60717-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60717-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="60717-118">-Name</span></span>
<span data-ttu-id="60717-119">Especifica o nome da conta de automação obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60717-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60717-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60717-120">-ResourceGroupName</span></span>
<span data-ttu-id="60717-121">Especifica o nome de um grupo de recursos em que este cmdlet obtém contas de automação.</span><span class="sxs-lookup"><span data-stu-id="60717-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60717-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60717-122">CommonParameters</span></span>
<span data-ttu-id="60717-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60717-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60717-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60717-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60717-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60717-125">INPUTS</span></span>

### <span data-ttu-id="60717-126">System. String</span><span class="sxs-lookup"><span data-stu-id="60717-126">System.String</span></span>

## <span data-ttu-id="60717-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60717-127">OUTPUTS</span></span>

### <span data-ttu-id="60717-128">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="60717-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="60717-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60717-129">NOTES</span></span>

## <span data-ttu-id="60717-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60717-130">RELATED LINKS</span></span>

[<span data-ttu-id="60717-131">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="60717-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="60717-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="60717-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="60717-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="60717-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


