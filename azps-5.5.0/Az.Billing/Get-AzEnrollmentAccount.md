---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112218"
---
# <span data-ttu-id="5c5a9-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="5c5a9-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="5c5a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c5a9-102">SYNOPSIS</span></span>
<span data-ttu-id="5c5a9-103">Obter contas de registro.</span><span class="sxs-lookup"><span data-stu-id="5c5a9-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="5c5a9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c5a9-104">SYNTAX</span></span>

### <span data-ttu-id="5c5a9-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5c5a9-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c5a9-106">Único</span><span class="sxs-lookup"><span data-stu-id="5c5a9-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c5a9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c5a9-107">DESCRIPTION</span></span>
<span data-ttu-id="5c5a9-108">O **cmdlet Get-AzEnrollmentAccount obtém** contas de registro.</span><span class="sxs-lookup"><span data-stu-id="5c5a9-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="5c5a9-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5c5a9-109">EXAMPLES</span></span>

### <span data-ttu-id="5c5a9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5c5a9-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="5c5a9-111">Obter todas as contas de registro disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5c5a9-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="5c5a9-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5c5a9-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="5c5a9-113">Obter a conta de registro com a ID de objeto especificada.</span><span class="sxs-lookup"><span data-stu-id="5c5a9-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="5c5a9-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c5a9-114">PARAMETERS</span></span>

### <span data-ttu-id="5c5a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c5a9-115">-DefaultProfile</span></span>
<span data-ttu-id="5c5a9-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5c5a9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c5a9-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5c5a9-117">-ObjectId</span></span>
<span data-ttu-id="5c5a9-118">ObjectId de uma conta de registro específica para obter.</span><span class="sxs-lookup"><span data-stu-id="5c5a9-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="5c5a9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c5a9-119">CommonParameters</span></span>
<span data-ttu-id="5c5a9-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c5a9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c5a9-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c5a9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c5a9-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="5c5a9-122">INPUTS</span></span>

### <span data-ttu-id="5c5a9-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5c5a9-123">None</span></span>

## <span data-ttu-id="5c5a9-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="5c5a9-124">OUTPUTS</span></span>

### <span data-ttu-id="5c5a9-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="5c5a9-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="5c5a9-126">Notas</span><span class="sxs-lookup"><span data-stu-id="5c5a9-126">NOTES</span></span>

## <span data-ttu-id="5c5a9-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c5a9-127">RELATED LINKS</span></span>
