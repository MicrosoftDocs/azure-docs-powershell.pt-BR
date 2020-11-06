---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: 48de3ae521f77c531433ffca67dadc9e2c46a980
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433312"
---
# <span data-ttu-id="6032f-101">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6032f-101">New-AzureRmBatchAccountKey</span></span>

## <span data-ttu-id="6032f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6032f-102">SYNOPSIS</span></span>
<span data-ttu-id="6032f-103">Regenera uma chave de uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="6032f-103">Regenerates a key of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6032f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6032f-104">SYNTAX</span></span>

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6032f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6032f-105">DESCRIPTION</span></span>
<span data-ttu-id="6032f-106">O cmdlet **New-AzureRmBatchAccountKey** regenera a chave primária ou secundária de uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="6032f-106">The **New-AzureRmBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="6032f-107">O cmdlet retorna um objeto **BatchAccountContext** que tem suas propriedades **PrimaryAccountKey** e **SecondaryAccountKey** atuais.</span><span class="sxs-lookup"><span data-stu-id="6032f-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="6032f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6032f-108">EXAMPLES</span></span>

### <span data-ttu-id="6032f-109">Exemplo 1: regenerar a chave da conta primária em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="6032f-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller

Location                     : westus

ResourceGroupName            : CmdletExampleRG

CoreQuota                    : 20

PoolQuota                    : 20

ActiveJobAndJobScheduleQuota : 20

Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="6032f-110">Esse comando regenera a chave da conta primária na conta em lotes chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="6032f-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="6032f-111">OS</span><span class="sxs-lookup"><span data-stu-id="6032f-111">PARAMETERS</span></span>

### <span data-ttu-id="6032f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6032f-112">-AccountName</span></span>
<span data-ttu-id="6032f-113">Especifica o nome da conta em lotes para a qual esse cmdlet regenera uma chave.</span><span class="sxs-lookup"><span data-stu-id="6032f-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6032f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6032f-114">-DefaultProfile</span></span>
<span data-ttu-id="6032f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6032f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6032f-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="6032f-116">-KeyType</span></span>
<span data-ttu-id="6032f-117">Especifica o tipo de chave que esse cmdlet regenera.</span><span class="sxs-lookup"><span data-stu-id="6032f-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="6032f-118">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="6032f-118">Valid values are:</span></span> 
- <span data-ttu-id="6032f-119">Preocupação</span><span class="sxs-lookup"><span data-stu-id="6032f-119">Primary</span></span>
- <span data-ttu-id="6032f-120">Segundo</span><span class="sxs-lookup"><span data-stu-id="6032f-120">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6032f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6032f-121">-ResourceGroupName</span></span>
<span data-ttu-id="6032f-122">Especifica o grupo de recursos da conta para a qual esse cmdlet regenera uma chave.</span><span class="sxs-lookup"><span data-stu-id="6032f-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6032f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6032f-123">CommonParameters</span></span>
<span data-ttu-id="6032f-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6032f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6032f-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6032f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6032f-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6032f-126">INPUTS</span></span>

### <span data-ttu-id="6032f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6032f-127">System.String</span></span>

## <span data-ttu-id="6032f-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6032f-128">OUTPUTS</span></span>

### <span data-ttu-id="6032f-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6032f-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6032f-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6032f-130">NOTES</span></span>

## <span data-ttu-id="6032f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6032f-131">RELATED LINKS</span></span>

[<span data-ttu-id="6032f-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6032f-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6032f-133">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="6032f-133">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

