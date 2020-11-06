---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 1f32e700cd5d0c20e041143e43755172ecf2da86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433313"
---
# <span data-ttu-id="092d8-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="092d8-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="092d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="092d8-102">SYNOPSIS</span></span>
<span data-ttu-id="092d8-103">Obtém as chaves de uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="092d8-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="092d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="092d8-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="092d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="092d8-105">DESCRIPTION</span></span>
<span data-ttu-id="092d8-106">O cmdlet **Get-AzureRmBatchAccountKeys** Obtém as chaves de uma conta em lotes do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="092d8-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="092d8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="092d8-107">EXAMPLES</span></span>

## <span data-ttu-id="092d8-108">OS</span><span class="sxs-lookup"><span data-stu-id="092d8-108">PARAMETERS</span></span>

### <span data-ttu-id="092d8-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="092d8-109">-AccountName</span></span>
<span data-ttu-id="092d8-110">Especifica o nome da conta para a qual esse cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="092d8-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="092d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="092d8-111">-DefaultProfile</span></span>
<span data-ttu-id="092d8-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="092d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="092d8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="092d8-113">-ResourceGroupName</span></span>
<span data-ttu-id="092d8-114">Especifica o nome do grupo de recursos que contém a conta para a qual esse cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="092d8-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="092d8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="092d8-115">CommonParameters</span></span>
<span data-ttu-id="092d8-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="092d8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="092d8-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="092d8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="092d8-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="092d8-118">INPUTS</span></span>

### <span data-ttu-id="092d8-119">System. String</span><span class="sxs-lookup"><span data-stu-id="092d8-119">System.String</span></span>

## <span data-ttu-id="092d8-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="092d8-120">OUTPUTS</span></span>

### <span data-ttu-id="092d8-121">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="092d8-121">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="092d8-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="092d8-122">NOTES</span></span>

## <span data-ttu-id="092d8-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="092d8-123">RELATED LINKS</span></span>

[<span data-ttu-id="092d8-124">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="092d8-124">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="092d8-125">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="092d8-125">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


