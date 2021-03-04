---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: e22c1ef6a95fafe21f0fd10a47a67098976395e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887229"
---
# <span data-ttu-id="762b4-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="762b4-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="762b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="762b4-102">SYNOPSIS</span></span>
<span data-ttu-id="762b4-103">Adiciona um aplicativo à conta Batch especificada.</span><span class="sxs-lookup"><span data-stu-id="762b4-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="762b4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="762b4-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="762b4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="762b4-105">DESCRIPTION</span></span>
<span data-ttu-id="762b4-106">O cmdlet **New-AzBatchApplication** adiciona um aplicativo à conta batch especificada do Azure.</span><span class="sxs-lookup"><span data-stu-id="762b4-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="762b4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="762b4-107">EXAMPLES</span></span>

### <span data-ttu-id="762b4-108">Exemplo 1: Adicionar um aplicativo vazio a uma conta Batch</span><span class="sxs-lookup"><span data-stu-id="762b4-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="762b4-109">Este comando cria o aplicativo Litware na conta ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="762b4-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="762b4-110">O aplicativo inicialmente não contém pacotes.</span><span class="sxs-lookup"><span data-stu-id="762b4-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="762b4-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="762b4-111">PARAMETERS</span></span>

### <span data-ttu-id="762b4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="762b4-112">-AccountName</span></span>
<span data-ttu-id="762b4-113">Especifica o nome da conta Batch à qual este cmdlet adiciona um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="762b4-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="762b4-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="762b4-114">-AllowUpdates</span></span>
<span data-ttu-id="762b4-115">Especifica se os pacotes dentro do aplicativo podem ser substituídos usando a mesma cadeia de caracteres de versão.</span><span class="sxs-lookup"><span data-stu-id="762b4-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762b4-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="762b4-116">-ApplicationName</span></span>
<span data-ttu-id="762b4-117">Especifica o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="762b4-117">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="762b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762b4-118">-DefaultProfile</span></span>
<span data-ttu-id="762b4-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="762b4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="762b4-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="762b4-120">-DisplayName</span></span>
<span data-ttu-id="762b4-121">Especifica o nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="762b4-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="762b4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="762b4-122">-ResourceGroupName</span></span>
<span data-ttu-id="762b4-123">Especifica o nome do grupo de recursos que contém a conta Batch.</span><span class="sxs-lookup"><span data-stu-id="762b4-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="762b4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762b4-124">CommonParameters</span></span>
<span data-ttu-id="762b4-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="762b4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762b4-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="762b4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762b4-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="762b4-127">INPUTS</span></span>

### <span data-ttu-id="762b4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="762b4-128">System.String</span></span>

### <span data-ttu-id="762b4-129">System.Nullable'1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="762b4-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="762b4-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="762b4-130">OUTPUTS</span></span>

### <span data-ttu-id="762b4-131">Microsoft.Azure.Commands.Batch. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="762b4-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="762b4-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="762b4-132">NOTES</span></span>

## <span data-ttu-id="762b4-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="762b4-133">RELATED LINKS</span></span>

[<span data-ttu-id="762b4-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="762b4-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="762b4-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="762b4-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="762b4-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="762b4-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="762b4-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="762b4-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="762b4-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="762b4-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="762b4-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="762b4-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


