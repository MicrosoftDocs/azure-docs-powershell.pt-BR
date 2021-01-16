---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260171"
---
# <span data-ttu-id="6c69a-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="6c69a-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="6c69a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c69a-102">SYNOPSIS</span></span>
<span data-ttu-id="6c69a-103">Obter contas de registro.</span><span class="sxs-lookup"><span data-stu-id="6c69a-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="6c69a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c69a-104">SYNTAX</span></span>

### <span data-ttu-id="6c69a-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="6c69a-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c69a-106">Apenas</span><span class="sxs-lookup"><span data-stu-id="6c69a-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c69a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c69a-107">DESCRIPTION</span></span>
<span data-ttu-id="6c69a-108">O cmdlet **Get-AzEnrollmentAccount** Obtém contas de registro.</span><span class="sxs-lookup"><span data-stu-id="6c69a-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="6c69a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c69a-109">EXAMPLES</span></span>

### <span data-ttu-id="6c69a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6c69a-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="6c69a-111">Obter todas as contas de registro disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6c69a-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="6c69a-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6c69a-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="6c69a-113">Obter a conta de registro com a ID de objeto especificada.</span><span class="sxs-lookup"><span data-stu-id="6c69a-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="6c69a-114">OS</span><span class="sxs-lookup"><span data-stu-id="6c69a-114">PARAMETERS</span></span>

### <span data-ttu-id="6c69a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c69a-115">-DefaultProfile</span></span>
<span data-ttu-id="6c69a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6c69a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c69a-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6c69a-117">-ObjectId</span></span>
<span data-ttu-id="6c69a-118">ObjectId de uma conta de Registro específica a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="6c69a-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="6c69a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c69a-119">CommonParameters</span></span>
<span data-ttu-id="6c69a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c69a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c69a-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c69a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c69a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c69a-122">INPUTS</span></span>

### <span data-ttu-id="6c69a-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6c69a-123">None</span></span>

## <span data-ttu-id="6c69a-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c69a-124">OUTPUTS</span></span>

### <span data-ttu-id="6c69a-125">Microsoft. Azure. Commands. billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="6c69a-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="6c69a-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c69a-126">NOTES</span></span>

## <span data-ttu-id="6c69a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c69a-127">RELATED LINKS</span></span>
