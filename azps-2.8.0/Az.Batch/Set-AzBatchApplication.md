---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
ms.openlocfilehash: d31c80a2da8e705c2515283ca219d05484e3c3dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597686"
---
# <span data-ttu-id="cfdd4-101">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="cfdd4-101">Set-AzBatchApplication</span></span>

## <span data-ttu-id="cfdd4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfdd4-102">SYNOPSIS</span></span>
<span data-ttu-id="cfdd4-103">Atualiza as configurações do aplicativo especificado.</span><span class="sxs-lookup"><span data-stu-id="cfdd4-103">Updates settings for the specified application.</span></span>

## <span data-ttu-id="cfdd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfdd4-104">SYNTAX</span></span>

```
Set-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfdd4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cfdd4-105">DESCRIPTION</span></span>
<span data-ttu-id="cfdd4-106">O cmdlet **set-AzBatchApplication** modifica as configurações do aplicativo em lotes do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="cfdd4-106">The **Set-AzBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="cfdd4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfdd4-107">EXAMPLES</span></span>

### <span data-ttu-id="cfdd4-108">Exemplo 1: atualizar um aplicativo em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="cfdd4-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="cfdd4-109">Esse comando altera se o aplicativo Litware na conta ContosoBatch permite atualizações.</span><span class="sxs-lookup"><span data-stu-id="cfdd4-109">This command changes whether the Litware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="cfdd4-110">O comando não altera a versão padrão ou o nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cfdd4-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="cfdd4-111">OS</span><span class="sxs-lookup"><span data-stu-id="cfdd4-111">PARAMETERS</span></span>

### <span data-ttu-id="cfdd4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cfdd4-112">-AccountName</span></span>
<span data-ttu-id="cfdd4-113">Especifica o nome da conta em lotes para a qual esse cmdlet modifica um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cfdd4-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="cfdd4-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="cfdd4-114">-AllowUpdates</span></span>
<span data-ttu-id="cfdd4-115">Especifica se os pacotes dentro do aplicativo podem ser substituídos usando a mesma cadeia de caracteres de versão.</span><span class="sxs-lookup"><span data-stu-id="cfdd4-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="cfdd4-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cfdd4-116">-ApplicationId</span></span>
<span data-ttu-id="cfdd4-117">Especifica a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cfdd4-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="cfdd4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfdd4-118">-DefaultProfile</span></span>
<span data-ttu-id="cfdd4-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cfdd4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfdd4-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="cfdd4-120">-DefaultVersion</span></span>
<span data-ttu-id="cfdd4-121">Especifica qual pacote usar se um cliente solicitar o aplicativo, mas não especificar uma versão.</span><span class="sxs-lookup"><span data-stu-id="cfdd4-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="cfdd4-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cfdd4-122">-DisplayName</span></span>
<span data-ttu-id="cfdd4-123">Especifica o nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cfdd4-123">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="cfdd4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfdd4-124">-ResourceGroupName</span></span>
<span data-ttu-id="cfdd4-125">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="cfdd4-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="cfdd4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfdd4-126">CommonParameters</span></span>
<span data-ttu-id="cfdd4-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfdd4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfdd4-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfdd4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfdd4-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cfdd4-129">INPUTS</span></span>

### <span data-ttu-id="cfdd4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cfdd4-130">System.String</span></span>

### <span data-ttu-id="cfdd4-131">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cfdd4-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cfdd4-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cfdd4-132">OUTPUTS</span></span>

### <span data-ttu-id="cfdd4-133">System. void</span><span class="sxs-lookup"><span data-stu-id="cfdd4-133">System.Void</span></span>

## <span data-ttu-id="cfdd4-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cfdd4-134">NOTES</span></span>

## <span data-ttu-id="cfdd4-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfdd4-135">RELATED LINKS</span></span>

[<span data-ttu-id="cfdd4-136">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="cfdd4-136">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="cfdd4-137">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="cfdd4-137">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="cfdd4-138">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="cfdd4-138">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="cfdd4-139">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="cfdd4-139">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="cfdd4-140">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="cfdd4-140">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="cfdd4-141">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="cfdd4-141">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)


