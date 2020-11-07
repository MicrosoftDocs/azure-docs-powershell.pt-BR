---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: f8da805a2c15356a4bf2188238b9a42a10617427
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785546"
---
# <span data-ttu-id="f853f-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f853f-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="f853f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f853f-102">SYNOPSIS</span></span>
<span data-ttu-id="f853f-103">Revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="f853f-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f853f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f853f-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f853f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f853f-105">DESCRIPTION</span></span>
<span data-ttu-id="f853f-106">O cmdlet **REVOKE-AzureRmDiskAccess** revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="f853f-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="f853f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f853f-107">EXAMPLES</span></span>

### <span data-ttu-id="f853f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f853f-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="f853f-109">Revogue o acesso ao disco chamado ' Disk01 ' no grupo de recursos chamado ' ResourceGroup01 '</span><span class="sxs-lookup"><span data-stu-id="f853f-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="f853f-110">OS</span><span class="sxs-lookup"><span data-stu-id="f853f-110">PARAMETERS</span></span>

### <span data-ttu-id="f853f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f853f-111">-AsJob</span></span>
<span data-ttu-id="f853f-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f853f-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f853f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f853f-113">-DefaultProfile</span></span>
<span data-ttu-id="f853f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f853f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f853f-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="f853f-115">-DiskName</span></span>
<span data-ttu-id="f853f-116">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="f853f-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f853f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f853f-117">-ResourceGroupName</span></span>
<span data-ttu-id="f853f-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f853f-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f853f-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f853f-119">-Confirm</span></span>
<span data-ttu-id="f853f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f853f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f853f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f853f-121">-WhatIf</span></span>
<span data-ttu-id="f853f-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f853f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f853f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f853f-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f853f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f853f-124">CommonParameters</span></span>
<span data-ttu-id="f853f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f853f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f853f-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f853f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f853f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f853f-127">INPUTS</span></span>

### <span data-ttu-id="f853f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f853f-128">System.String</span></span>

## <span data-ttu-id="f853f-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f853f-129">OUTPUTS</span></span>

### <span data-ttu-id="f853f-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="f853f-130">System.Object</span></span>

## <span data-ttu-id="f853f-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f853f-131">NOTES</span></span>

## <span data-ttu-id="f853f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f853f-132">RELATED LINKS</span></span>

