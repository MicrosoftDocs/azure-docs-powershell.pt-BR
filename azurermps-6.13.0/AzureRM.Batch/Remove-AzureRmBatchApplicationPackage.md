---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 7d8552ccc2c293f33c71402043a28bfad32ceeeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427287"
---
# <span data-ttu-id="33192-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="33192-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="33192-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33192-102">SYNOPSIS</span></span>
<span data-ttu-id="33192-103">Exclui um registro de pacote de aplicativo e o arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="33192-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33192-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33192-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33192-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33192-105">DESCRIPTION</span></span>
<span data-ttu-id="33192-106">O cmdlet **Remove-AzureRmBatchApplicationPackage** exclui um registro de pacote de aplicativo e o arquivo binário de uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="33192-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="33192-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33192-107">EXAMPLES</span></span>

### <span data-ttu-id="33192-108">Exemplo 1: excluir um pacote de aplicativo de uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="33192-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="33192-109">Este comando exclui a versão 1,0 do aplicativo Litware da conta ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="33192-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="33192-110">O comando exclui o registro do pacote e o blob que contêm o arquivo binário do pacote.</span><span class="sxs-lookup"><span data-stu-id="33192-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="33192-111">OS</span><span class="sxs-lookup"><span data-stu-id="33192-111">PARAMETERS</span></span>

### <span data-ttu-id="33192-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="33192-112">-AccountName</span></span>
<span data-ttu-id="33192-113">Especifica o nome da conta em lotes da qual esse cmdlet exclui um pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="33192-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="33192-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="33192-114">-ApplicationId</span></span>
<span data-ttu-id="33192-115">Especifica a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="33192-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="33192-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="33192-116">-ApplicationVersion</span></span>
<span data-ttu-id="33192-117">Especifica a versão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="33192-117">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33192-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33192-118">-DefaultProfile</span></span>
<span data-ttu-id="33192-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33192-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33192-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33192-120">-ResourceGroupName</span></span>
<span data-ttu-id="33192-121">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="33192-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="33192-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33192-122">CommonParameters</span></span>
<span data-ttu-id="33192-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33192-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33192-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33192-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33192-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33192-125">INPUTS</span></span>

### <span data-ttu-id="33192-126">System. String</span><span class="sxs-lookup"><span data-stu-id="33192-126">System.String</span></span>

## <span data-ttu-id="33192-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33192-127">OUTPUTS</span></span>

### <span data-ttu-id="33192-128">System. void</span><span class="sxs-lookup"><span data-stu-id="33192-128">System.Void</span></span>

## <span data-ttu-id="33192-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33192-129">NOTES</span></span>

## <span data-ttu-id="33192-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33192-130">RELATED LINKS</span></span>

[<span data-ttu-id="33192-131">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="33192-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="33192-132">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="33192-132">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="33192-133">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="33192-133">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="33192-134">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="33192-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="33192-135">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="33192-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="33192-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="33192-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)

