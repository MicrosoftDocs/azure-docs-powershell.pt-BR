---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: ae45dadd2d5af2cf81a8735ca6725ee4798dbf29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432050"
---
# <span data-ttu-id="51a74-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="51a74-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="51a74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51a74-102">SYNOPSIS</span></span>
<span data-ttu-id="51a74-103">Concede um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="51a74-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51a74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51a74-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51a74-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51a74-105">DESCRIPTION</span></span>
<span data-ttu-id="51a74-106">O cmdlet **Grant-AzureRmDiskAccess** concede um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="51a74-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="51a74-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51a74-107">EXAMPLES</span></span>

### <span data-ttu-id="51a74-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="51a74-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="51a74-109">Conceda o acesso "leitura" ao disco chamado "Disk01" no grupo de recursos chamado "ResourceGroup01" por 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="51a74-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="51a74-110">OS</span><span class="sxs-lookup"><span data-stu-id="51a74-110">PARAMETERS</span></span>

### <span data-ttu-id="51a74-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="51a74-111">-Access</span></span>
<span data-ttu-id="51a74-112">Especifica o nível de acesso.</span><span class="sxs-lookup"><span data-stu-id="51a74-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51a74-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51a74-113">-AsJob</span></span>
<span data-ttu-id="51a74-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="51a74-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51a74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a74-115">-DefaultProfile</span></span>
<span data-ttu-id="51a74-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51a74-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51a74-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="51a74-117">-DiskName</span></span>
<span data-ttu-id="51a74-118">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="51a74-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="51a74-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="51a74-119">-DurationInSecond</span></span>
<span data-ttu-id="51a74-120">Especifica a duração do acesso em segundos.</span><span class="sxs-lookup"><span data-stu-id="51a74-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51a74-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51a74-121">-ResourceGroupName</span></span>
<span data-ttu-id="51a74-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="51a74-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="51a74-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="51a74-123">-Confirm</span></span>
<span data-ttu-id="51a74-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51a74-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51a74-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51a74-125">-WhatIf</span></span>
<span data-ttu-id="51a74-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51a74-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51a74-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51a74-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51a74-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a74-128">CommonParameters</span></span>
<span data-ttu-id="51a74-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51a74-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a74-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51a74-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a74-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51a74-131">INPUTS</span></span>

### <span data-ttu-id="51a74-132">System. String</span><span class="sxs-lookup"><span data-stu-id="51a74-132">System.String</span></span>

## <span data-ttu-id="51a74-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51a74-133">OUTPUTS</span></span>

### <span data-ttu-id="51a74-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="51a74-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="51a74-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51a74-135">NOTES</span></span>

## <span data-ttu-id="51a74-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51a74-136">RELATED LINKS</span></span>