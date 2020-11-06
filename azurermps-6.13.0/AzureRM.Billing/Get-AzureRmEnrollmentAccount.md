---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d5d43a0aebcc553a230655d52399081548aae209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609851"
---
# <span data-ttu-id="4aeaa-101">Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="4aeaa-101">Get-AzureRmEnrollmentAccount</span></span>

## <span data-ttu-id="4aeaa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4aeaa-102">SYNOPSIS</span></span>
<span data-ttu-id="4aeaa-103">Obter contas de registro.</span><span class="sxs-lookup"><span data-stu-id="4aeaa-103">Get enrollment accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aeaa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4aeaa-104">SYNTAX</span></span>

### <span data-ttu-id="4aeaa-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="4aeaa-105">List (Default)</span></span>
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aeaa-106">Apenas</span><span class="sxs-lookup"><span data-stu-id="4aeaa-106">Single</span></span>
```
Get-AzureRmEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4aeaa-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4aeaa-107">DESCRIPTION</span></span>
<span data-ttu-id="4aeaa-108">O cmdlet **Get-AzureRmEnrollmentAccount** Obtém contas de registro.</span><span class="sxs-lookup"><span data-stu-id="4aeaa-108">The **Get-AzureRmEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="4aeaa-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4aeaa-109">EXAMPLES</span></span>

### <span data-ttu-id="4aeaa-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4aeaa-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="4aeaa-111">Obter todas as contas de registro disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4aeaa-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="4aeaa-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4aeaa-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="4aeaa-113">Obter a conta de registro com a ID de objeto especificada.</span><span class="sxs-lookup"><span data-stu-id="4aeaa-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="4aeaa-114">OS</span><span class="sxs-lookup"><span data-stu-id="4aeaa-114">PARAMETERS</span></span>

### <span data-ttu-id="4aeaa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aeaa-115">-DefaultProfile</span></span>
<span data-ttu-id="4aeaa-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4aeaa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4aeaa-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4aeaa-117">-ObjectId</span></span>
<span data-ttu-id="4aeaa-118">ObjectId de uma conta de Registro específica a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="4aeaa-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="4aeaa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aeaa-119">CommonParameters</span></span>
<span data-ttu-id="4aeaa-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aeaa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aeaa-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aeaa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aeaa-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4aeaa-122">INPUTS</span></span>

### <span data-ttu-id="4aeaa-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4aeaa-123">None</span></span>

## <span data-ttu-id="4aeaa-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4aeaa-124">OUTPUTS</span></span>

### <span data-ttu-id="4aeaa-125">Microsoft. Azure. Commands. billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="4aeaa-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="4aeaa-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4aeaa-126">NOTES</span></span>

## <span data-ttu-id="4aeaa-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4aeaa-127">RELATED LINKS</span></span>
