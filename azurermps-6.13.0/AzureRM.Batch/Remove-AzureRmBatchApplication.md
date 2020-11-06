---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
ms.openlocfilehash: 61288340bb2b9acb2bd47388d8f776d5c732b6f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427288"
---
# <span data-ttu-id="0f126-101">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0f126-101">Remove-AzureRmBatchApplication</span></span>

## <span data-ttu-id="0f126-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f126-102">SYNOPSIS</span></span>
<span data-ttu-id="0f126-103">Exclui um aplicativo de uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="0f126-103">Deletes an application from a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f126-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f126-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f126-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f126-105">DESCRIPTION</span></span>
<span data-ttu-id="0f126-106">O cmdlet **Remove-AzureRmBatchApplication** exclui um aplicativo de uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f126-106">The **Remove-AzureRmBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="0f126-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f126-107">EXAMPLES</span></span>

### <span data-ttu-id="0f126-108">Exemplo 1: excluir um aplicativo de uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="0f126-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="0f126-109">Esse comando exclui o aplicativo Litware da conta ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="0f126-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="0f126-110">O comando falhará se o aplicativo contiver pacotes.</span><span class="sxs-lookup"><span data-stu-id="0f126-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="0f126-111">OS</span><span class="sxs-lookup"><span data-stu-id="0f126-111">PARAMETERS</span></span>

### <span data-ttu-id="0f126-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0f126-112">-AccountName</span></span>
<span data-ttu-id="0f126-113">Especifica o nome da conta em lotes da qual esse cmdlet Remove um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f126-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f126-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0f126-114">-ApplicationId</span></span>
<span data-ttu-id="0f126-115">Especifica a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f126-115">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f126-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f126-116">-DefaultProfile</span></span>
<span data-ttu-id="0f126-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f126-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f126-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f126-118">-ResourceGroupName</span></span>
<span data-ttu-id="0f126-119">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="0f126-119">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f126-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f126-120">CommonParameters</span></span>
<span data-ttu-id="0f126-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f126-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f126-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f126-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f126-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f126-123">INPUTS</span></span>

### <span data-ttu-id="0f126-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0f126-124">System.String</span></span>

## <span data-ttu-id="0f126-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f126-125">OUTPUTS</span></span>

### <span data-ttu-id="0f126-126">System. void</span><span class="sxs-lookup"><span data-stu-id="0f126-126">System.Void</span></span>

## <span data-ttu-id="0f126-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f126-127">NOTES</span></span>

## <span data-ttu-id="0f126-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f126-128">RELATED LINKS</span></span>

[<span data-ttu-id="0f126-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0f126-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="0f126-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0f126-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="0f126-131">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0f126-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="0f126-132">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0f126-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="0f126-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0f126-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="0f126-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0f126-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)

