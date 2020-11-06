---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 8e6e10c45034402e5339ed5cb6d60a9319362450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426818"
---
# <span data-ttu-id="b6e59-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b6e59-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="b6e59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6e59-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e59-103">Obtém as chaves de uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="b6e59-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6e59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6e59-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6e59-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6e59-105">DESCRIPTION</span></span>
<span data-ttu-id="b6e59-106">O cmdlet **Get-AzureRmBatchAccountKeys** Obtém as chaves de uma conta em lotes do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="b6e59-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="b6e59-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6e59-107">EXAMPLES</span></span>

## <span data-ttu-id="b6e59-108">OS</span><span class="sxs-lookup"><span data-stu-id="b6e59-108">PARAMETERS</span></span>

### <span data-ttu-id="b6e59-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6e59-109">-AccountName</span></span>
<span data-ttu-id="b6e59-110">Especifica o nome da conta para a qual esse cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="b6e59-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e59-111">-DefaultProfile</span></span>
<span data-ttu-id="b6e59-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6e59-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e59-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6e59-113">-ResourceGroupName</span></span>
<span data-ttu-id="b6e59-114">Especifica o nome do grupo de recursos que contém a conta para a qual esse cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="b6e59-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e59-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e59-115">CommonParameters</span></span>
<span data-ttu-id="b6e59-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6e59-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e59-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6e59-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e59-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6e59-118">INPUTS</span></span>

### <span data-ttu-id="b6e59-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b6e59-119">None</span></span>
<span data-ttu-id="b6e59-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b6e59-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6e59-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6e59-121">OUTPUTS</span></span>

### <span data-ttu-id="b6e59-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b6e59-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b6e59-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6e59-123">NOTES</span></span>

## <span data-ttu-id="b6e59-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6e59-124">RELATED LINKS</span></span>

[<span data-ttu-id="b6e59-125">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b6e59-125">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="b6e59-126">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="b6e59-126">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


