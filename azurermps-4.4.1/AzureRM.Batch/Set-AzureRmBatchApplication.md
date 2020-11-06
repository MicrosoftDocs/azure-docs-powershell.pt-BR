---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: c1170dc6413c615c7ea1941cc9a446fe2da1610b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431132"
---
# <span data-ttu-id="293ca-101">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="293ca-101">Set-AzureRmBatchApplication</span></span>

## <span data-ttu-id="293ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="293ca-102">SYNOPSIS</span></span>
<span data-ttu-id="293ca-103">Atualiza as configurações do aplicativo especificado.</span><span class="sxs-lookup"><span data-stu-id="293ca-103">Updates settings for the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="293ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="293ca-104">SYNTAX</span></span>

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="293ca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="293ca-105">DESCRIPTION</span></span>
<span data-ttu-id="293ca-106">O cmdlet **set-AzureRmBatchApplication** modifica as configurações do aplicativo em lotes do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="293ca-106">The **Set-AzureRmBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="293ca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="293ca-107">EXAMPLES</span></span>

### <span data-ttu-id="293ca-108">Exemplo 1: atualizar um aplicativo em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="293ca-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="293ca-109">Esse comando altera se o aplicativo Llitware na conta ContosoBatch permite atualizações.</span><span class="sxs-lookup"><span data-stu-id="293ca-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="293ca-110">O comando não altera a versão padrão ou o nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="293ca-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="293ca-111">OS</span><span class="sxs-lookup"><span data-stu-id="293ca-111">PARAMETERS</span></span>

### <span data-ttu-id="293ca-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="293ca-112">-AccountName</span></span>
<span data-ttu-id="293ca-113">Especifica o nome da conta em lotes para a qual esse cmdlet modifica um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="293ca-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="293ca-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="293ca-114">-AllowUpdates</span></span>
<span data-ttu-id="293ca-115">Especifica se os pacotes dentro do aplicativo podem ser substituídos usando a mesma cadeia de caracteres de versão.</span><span class="sxs-lookup"><span data-stu-id="293ca-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="293ca-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="293ca-116">-ApplicationId</span></span>
<span data-ttu-id="293ca-117">Especifica a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="293ca-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="293ca-118">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="293ca-118">-DefaultVersion</span></span>
<span data-ttu-id="293ca-119">Especifica qual pacote usar se um cliente solicitar o aplicativo, mas não especificar uma versão.</span><span class="sxs-lookup"><span data-stu-id="293ca-119">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="293ca-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="293ca-120">-DisplayName</span></span>
<span data-ttu-id="293ca-121">Especifica o nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="293ca-121">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="293ca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="293ca-122">-ResourceGroupName</span></span>
<span data-ttu-id="293ca-123">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="293ca-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="293ca-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293ca-124">-DefaultProfile</span></span>
<span data-ttu-id="293ca-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="293ca-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="293ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293ca-126">CommonParameters</span></span>
<span data-ttu-id="293ca-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="293ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293ca-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="293ca-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293ca-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="293ca-129">INPUTS</span></span>

## <span data-ttu-id="293ca-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="293ca-130">OUTPUTS</span></span>

## <span data-ttu-id="293ca-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="293ca-131">NOTES</span></span>

## <span data-ttu-id="293ca-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="293ca-132">RELATED LINKS</span></span>

[<span data-ttu-id="293ca-133">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="293ca-133">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="293ca-134">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="293ca-134">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="293ca-135">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="293ca-135">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="293ca-136">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="293ca-136">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="293ca-137">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="293ca-137">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="293ca-138">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="293ca-138">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

