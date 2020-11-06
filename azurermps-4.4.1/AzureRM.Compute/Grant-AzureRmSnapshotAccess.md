---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: 9b870214362c6e2bcd7225ef5a40ed5ff780139a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430758"
---
# <span data-ttu-id="0863a-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="0863a-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="0863a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0863a-102">SYNOPSIS</span></span>
<span data-ttu-id="0863a-103">Concede um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="0863a-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0863a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0863a-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0863a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0863a-105">DESCRIPTION</span></span>
<span data-ttu-id="0863a-106">O cmdlet **Grant-AzureRmSnapshotAccess** concede um acesso a um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="0863a-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="0863a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0863a-107">EXAMPLES</span></span>

### <span data-ttu-id="0863a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0863a-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="0863a-109">Conceda acesso "leitura" ao instantâneo chamado "Snapshot01" no grupo de recursos chamado "ResourceGroup01" para 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="0863a-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="0863a-110">OS</span><span class="sxs-lookup"><span data-stu-id="0863a-110">PARAMETERS</span></span>

### <span data-ttu-id="0863a-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="0863a-111">-Access</span></span>
<span data-ttu-id="0863a-112">Especifica o nível de acesso.</span><span class="sxs-lookup"><span data-stu-id="0863a-112">Specifies Access level.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0863a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0863a-113">-DefaultProfile</span></span>
<span data-ttu-id="0863a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0863a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0863a-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="0863a-115">-DurationInSecond</span></span>
<span data-ttu-id="0863a-116">Especifica a duração do acesso em segundos.</span><span class="sxs-lookup"><span data-stu-id="0863a-116">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="0863a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0863a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0863a-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0863a-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0863a-119">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="0863a-119">-SnapshotName</span></span>
<span data-ttu-id="0863a-120">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="0863a-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="0863a-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0863a-121">-Confirm</span></span>
<span data-ttu-id="0863a-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0863a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0863a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0863a-123">-WhatIf</span></span>
<span data-ttu-id="0863a-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0863a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0863a-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0863a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0863a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0863a-126">CommonParameters</span></span>
<span data-ttu-id="0863a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0863a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0863a-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0863a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0863a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0863a-129">INPUTS</span></span>

### <span data-ttu-id="0863a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0863a-130">System.String</span></span>

## <span data-ttu-id="0863a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0863a-131">OUTPUTS</span></span>

### <span data-ttu-id="0863a-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="0863a-132">System.Object</span></span>

## <span data-ttu-id="0863a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0863a-133">NOTES</span></span>

## <span data-ttu-id="0863a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0863a-134">RELATED LINKS</span></span>

