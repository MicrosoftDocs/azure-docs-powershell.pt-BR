---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262804"
---
# <span data-ttu-id="3a55e-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3a55e-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="3a55e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a55e-102">SYNOPSIS</span></span>
<span data-ttu-id="3a55e-103">Exclui um registro de pacote de aplicativo e o arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="3a55e-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="3a55e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a55e-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a55e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a55e-105">DESCRIPTION</span></span>
<span data-ttu-id="3a55e-106">O cmdlet **Remove-AzBatchApplicationPackage** exclui um registro de pacote de aplicativo e o arquivo binário de uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a55e-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="3a55e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a55e-107">EXAMPLES</span></span>

### <span data-ttu-id="3a55e-108">Exemplo 1: excluir um pacote de aplicativo de uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="3a55e-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="3a55e-109">Este comando exclui a versão 1,0 do aplicativo Litware da conta ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="3a55e-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="3a55e-110">O comando exclui o registro do pacote e o blob que contêm o arquivo binário do pacote.</span><span class="sxs-lookup"><span data-stu-id="3a55e-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="3a55e-111">OS</span><span class="sxs-lookup"><span data-stu-id="3a55e-111">PARAMETERS</span></span>

### <span data-ttu-id="3a55e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3a55e-112">-AccountName</span></span>
<span data-ttu-id="3a55e-113">Especifica o nome da conta em lotes da qual esse cmdlet exclui um pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3a55e-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="3a55e-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="3a55e-114">-ApplicationName</span></span>
<span data-ttu-id="3a55e-115">Especifica o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3a55e-115">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a55e-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="3a55e-116">-ApplicationVersion</span></span>
<span data-ttu-id="3a55e-117">Especifica a versão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3a55e-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="3a55e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a55e-118">-DefaultProfile</span></span>
<span data-ttu-id="3a55e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a55e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a55e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a55e-120">-ResourceGroupName</span></span>
<span data-ttu-id="3a55e-121">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="3a55e-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="3a55e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a55e-122">CommonParameters</span></span>
<span data-ttu-id="3a55e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a55e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a55e-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a55e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a55e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a55e-125">INPUTS</span></span>

### <span data-ttu-id="3a55e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3a55e-126">System.String</span></span>

## <span data-ttu-id="3a55e-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a55e-127">OUTPUTS</span></span>

### <span data-ttu-id="3a55e-128">System. void</span><span class="sxs-lookup"><span data-stu-id="3a55e-128">System.Void</span></span>

## <span data-ttu-id="3a55e-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a55e-129">NOTES</span></span>

## <span data-ttu-id="3a55e-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a55e-130">RELATED LINKS</span></span>

[<span data-ttu-id="3a55e-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3a55e-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="3a55e-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3a55e-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="3a55e-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3a55e-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="3a55e-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3a55e-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="3a55e-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3a55e-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="3a55e-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3a55e-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


