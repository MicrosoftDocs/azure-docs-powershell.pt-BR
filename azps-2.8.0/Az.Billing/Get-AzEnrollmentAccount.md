---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d76797f82a14c8efa2f9a3d6a77436fa2f8a1b68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597656"
---
# <span data-ttu-id="0ebec-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="0ebec-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="0ebec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ebec-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebec-103">Obter contas de registro.</span><span class="sxs-lookup"><span data-stu-id="0ebec-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="0ebec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ebec-104">SYNTAX</span></span>

### <span data-ttu-id="0ebec-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="0ebec-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ebec-106">Apenas</span><span class="sxs-lookup"><span data-stu-id="0ebec-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ebec-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0ebec-107">DESCRIPTION</span></span>
<span data-ttu-id="0ebec-108">O cmdlet **Get-AzEnrollmentAccount** Obtém contas de registro.</span><span class="sxs-lookup"><span data-stu-id="0ebec-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="0ebec-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ebec-109">EXAMPLES</span></span>

### <span data-ttu-id="0ebec-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0ebec-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="0ebec-111">Obter todas as contas de registro disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0ebec-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="0ebec-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0ebec-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="0ebec-113">Obter a conta de registro com a ID de objeto especificada.</span><span class="sxs-lookup"><span data-stu-id="0ebec-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="0ebec-114">OS</span><span class="sxs-lookup"><span data-stu-id="0ebec-114">PARAMETERS</span></span>

### <span data-ttu-id="0ebec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebec-115">-DefaultProfile</span></span>
<span data-ttu-id="0ebec-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0ebec-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ebec-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0ebec-117">-ObjectId</span></span>
<span data-ttu-id="0ebec-118">ObjectId de uma conta de Registro específica a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="0ebec-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="0ebec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebec-119">CommonParameters</span></span>
<span data-ttu-id="0ebec-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebec-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ebec-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebec-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0ebec-122">INPUTS</span></span>

### <span data-ttu-id="0ebec-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0ebec-123">None</span></span>

## <span data-ttu-id="0ebec-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0ebec-124">OUTPUTS</span></span>

### <span data-ttu-id="0ebec-125">Microsoft. Azure. Commands. billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="0ebec-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="0ebec-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0ebec-126">NOTES</span></span>

## <span data-ttu-id="0ebec-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ebec-127">RELATED LINKS</span></span>
