---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: e079701f0d2ccca49e1368edc9446c08b4549c11
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93947217"
---
# <span data-ttu-id="042ed-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="042ed-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="042ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="042ed-102">SYNOPSIS</span></span>
<span data-ttu-id="042ed-103">Regenera uma chave de uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="042ed-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="042ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="042ed-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="042ed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="042ed-105">DESCRIPTION</span></span>
<span data-ttu-id="042ed-106">O cmdlet **New-AzBatchAccountKey** regenera a chave primária ou secundária de uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="042ed-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="042ed-107">O cmdlet retorna um objeto **BatchAccountContext** que tem suas propriedades **PrimaryAccountKey** e **SecondaryAccountKey** atuais.</span><span class="sxs-lookup"><span data-stu-id="042ed-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="042ed-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="042ed-108">EXAMPLES</span></span>

### <span data-ttu-id="042ed-109">Exemplo 1: regenerar a chave da conta primária em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="042ed-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
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

<span data-ttu-id="042ed-110">Esse comando regenera a chave da conta primária na conta em lotes chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="042ed-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="042ed-111">OS</span><span class="sxs-lookup"><span data-stu-id="042ed-111">PARAMETERS</span></span>

### <span data-ttu-id="042ed-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="042ed-112">-AccountName</span></span>
<span data-ttu-id="042ed-113">Especifica o nome da conta em lotes para a qual esse cmdlet regenera uma chave.</span><span class="sxs-lookup"><span data-stu-id="042ed-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="042ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="042ed-114">-DefaultProfile</span></span>
<span data-ttu-id="042ed-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="042ed-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="042ed-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="042ed-116">-KeyType</span></span>
<span data-ttu-id="042ed-117">Especifica o tipo de chave que esse cmdlet regenera.</span><span class="sxs-lookup"><span data-stu-id="042ed-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="042ed-118">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="042ed-118">Valid values are:</span></span> 
- <span data-ttu-id="042ed-119">Preocupação</span><span class="sxs-lookup"><span data-stu-id="042ed-119">Primary</span></span>
- <span data-ttu-id="042ed-120">Segundo</span><span class="sxs-lookup"><span data-stu-id="042ed-120">Secondary</span></span>

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

### <span data-ttu-id="042ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="042ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="042ed-122">Especifica o grupo de recursos da conta para a qual esse cmdlet regenera uma chave.</span><span class="sxs-lookup"><span data-stu-id="042ed-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="042ed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="042ed-123">CommonParameters</span></span>
<span data-ttu-id="042ed-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="042ed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="042ed-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="042ed-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="042ed-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="042ed-126">INPUTS</span></span>

### <span data-ttu-id="042ed-127">System. String</span><span class="sxs-lookup"><span data-stu-id="042ed-127">System.String</span></span>

## <span data-ttu-id="042ed-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="042ed-128">OUTPUTS</span></span>

### <span data-ttu-id="042ed-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="042ed-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="042ed-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="042ed-130">NOTES</span></span>

## <span data-ttu-id="042ed-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="042ed-131">RELATED LINKS</span></span>

[<span data-ttu-id="042ed-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="042ed-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="042ed-133">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="042ed-133">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


