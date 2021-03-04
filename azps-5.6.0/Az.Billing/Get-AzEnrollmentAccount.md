---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d05499ded326787b9930574872dd0681f773d1c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890655"
---
# <span data-ttu-id="a1c60-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="a1c60-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="a1c60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1c60-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c60-103">Obter contas de registro.</span><span class="sxs-lookup"><span data-stu-id="a1c60-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="a1c60-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a1c60-104">SYNTAX</span></span>

### <span data-ttu-id="a1c60-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a1c60-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1c60-106">Single</span><span class="sxs-lookup"><span data-stu-id="a1c60-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1c60-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a1c60-107">DESCRIPTION</span></span>
<span data-ttu-id="a1c60-108">O cmdlet **Get-AzEnrollmentAccount** obtém contas de registro.</span><span class="sxs-lookup"><span data-stu-id="a1c60-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="a1c60-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1c60-109">EXAMPLES</span></span>

### <span data-ttu-id="a1c60-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1c60-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="a1c60-111">Obter todas as contas de registro disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a1c60-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="a1c60-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a1c60-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="a1c60-113">Obter a conta de registro com a ID do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="a1c60-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="a1c60-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a1c60-114">PARAMETERS</span></span>

### <span data-ttu-id="a1c60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c60-115">-DefaultProfile</span></span>
<span data-ttu-id="a1c60-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a1c60-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1c60-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a1c60-117">-ObjectId</span></span>
<span data-ttu-id="a1c60-118">ObjectId de uma conta de registro específica para obter.</span><span class="sxs-lookup"><span data-stu-id="a1c60-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c60-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c60-119">CommonParameters</span></span>
<span data-ttu-id="a1c60-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c60-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c60-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c60-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c60-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1c60-122">INPUTS</span></span>

### <span data-ttu-id="a1c60-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a1c60-123">None</span></span>

## <span data-ttu-id="a1c60-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a1c60-124">OUTPUTS</span></span>

### <span data-ttu-id="a1c60-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="a1c60-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="a1c60-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="a1c60-126">NOTES</span></span>

## <span data-ttu-id="a1c60-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1c60-127">RELATED LINKS</span></span>
