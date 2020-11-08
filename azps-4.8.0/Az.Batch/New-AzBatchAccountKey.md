---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: 121e4b4b2ffe25d9e5ae53cb03e60cb7a1da91b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110622"
---
# <span data-ttu-id="d08bf-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d08bf-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="d08bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d08bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d08bf-103">Regenera uma chave de uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="d08bf-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="d08bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d08bf-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d08bf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d08bf-105">DESCRIPTION</span></span>
<span data-ttu-id="d08bf-106">O cmdlet **New-AzBatchAccountKey** regenera a chave primária ou secundária de uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="d08bf-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="d08bf-107">O cmdlet retorna um objeto **BatchAccountContext** que tem suas propriedades **PrimaryAccountKey** e **SecondaryAccountKey** atuais.</span><span class="sxs-lookup"><span data-stu-id="d08bf-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="d08bf-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d08bf-108">EXAMPLES</span></span>

### <span data-ttu-id="d08bf-109">Exemplo 1: regenerar a chave da conta primária em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="d08bf-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="d08bf-110">Esse comando regenera a chave da conta primária na conta em lotes chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="d08bf-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="d08bf-111">OS</span><span class="sxs-lookup"><span data-stu-id="d08bf-111">PARAMETERS</span></span>

### <span data-ttu-id="d08bf-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d08bf-112">-AccountName</span></span>
<span data-ttu-id="d08bf-113">Especifica o nome da conta em lotes para a qual esse cmdlet regenera uma chave.</span><span class="sxs-lookup"><span data-stu-id="d08bf-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="d08bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d08bf-114">-DefaultProfile</span></span>
<span data-ttu-id="d08bf-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d08bf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d08bf-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="d08bf-116">-KeyType</span></span>
<span data-ttu-id="d08bf-117">Especifica o tipo de chave que esse cmdlet regenera.</span><span class="sxs-lookup"><span data-stu-id="d08bf-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="d08bf-118">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="d08bf-118">Valid values are:</span></span>
- <span data-ttu-id="d08bf-119">Preocupação</span><span class="sxs-lookup"><span data-stu-id="d08bf-119">Primary</span></span>
- <span data-ttu-id="d08bf-120">Segundo</span><span class="sxs-lookup"><span data-stu-id="d08bf-120">Secondary</span></span>

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

### <span data-ttu-id="d08bf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d08bf-121">-ResourceGroupName</span></span>
<span data-ttu-id="d08bf-122">Especifica o grupo de recursos da conta para a qual esse cmdlet regenera uma chave.</span><span class="sxs-lookup"><span data-stu-id="d08bf-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="d08bf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d08bf-123">CommonParameters</span></span>
<span data-ttu-id="d08bf-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d08bf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d08bf-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d08bf-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d08bf-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d08bf-126">INPUTS</span></span>

### <span data-ttu-id="d08bf-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d08bf-127">System.String</span></span>

## <span data-ttu-id="d08bf-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d08bf-128">OUTPUTS</span></span>

### <span data-ttu-id="d08bf-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d08bf-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d08bf-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d08bf-130">NOTES</span></span>

## <span data-ttu-id="d08bf-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d08bf-131">RELATED LINKS</span></span>

[<span data-ttu-id="d08bf-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d08bf-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d08bf-133">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="d08bf-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
