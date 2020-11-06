---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: eb71d1a74e68bdf4157cacd4b87aa9a05bdc00db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426411"
---
# <span data-ttu-id="9b9cf-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="9b9cf-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="9b9cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="9b9cf-103">Revoga um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="9b9cf-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b9cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b9cf-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b9cf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b9cf-105">DESCRIPTION</span></span>
<span data-ttu-id="9b9cf-106">O cmdlet **REVOKE-AzureRmSnapshotAccess** revoga um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="9b9cf-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="9b9cf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b9cf-107">EXAMPLES</span></span>

### <span data-ttu-id="9b9cf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b9cf-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="9b9cf-109">Revogue o acesso ao instantâneo chamado ' Snapshot01 ' no grupo de recursos chamado ' ResourceGroup01 '</span><span class="sxs-lookup"><span data-stu-id="9b9cf-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="9b9cf-110">OS</span><span class="sxs-lookup"><span data-stu-id="9b9cf-110">PARAMETERS</span></span>

### <span data-ttu-id="9b9cf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b9cf-111">-AsJob</span></span>
<span data-ttu-id="9b9cf-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9b9cf-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b9cf-113">-DefaultProfile</span></span>
<span data-ttu-id="9b9cf-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b9cf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b9cf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b9cf-115">-ResourceGroupName</span></span>
<span data-ttu-id="9b9cf-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9b9cf-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9b9cf-117">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="9b9cf-117">-SnapshotName</span></span>
<span data-ttu-id="9b9cf-118">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="9b9cf-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b9cf-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9b9cf-119">-Confirm</span></span>
<span data-ttu-id="9b9cf-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b9cf-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9cf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b9cf-121">-WhatIf</span></span>
<span data-ttu-id="9b9cf-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b9cf-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b9cf-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b9cf-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b9cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b9cf-124">CommonParameters</span></span>
<span data-ttu-id="9b9cf-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b9cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b9cf-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b9cf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b9cf-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b9cf-127">INPUTS</span></span>

### <span data-ttu-id="9b9cf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9b9cf-128">System.String</span></span>

## <span data-ttu-id="9b9cf-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b9cf-129">OUTPUTS</span></span>

### <span data-ttu-id="9b9cf-130">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9b9cf-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9b9cf-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b9cf-131">NOTES</span></span>

## <span data-ttu-id="9b9cf-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b9cf-132">RELATED LINKS</span></span>
