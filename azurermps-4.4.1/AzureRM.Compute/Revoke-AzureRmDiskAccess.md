---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 58cbbfd2314589fd6b28f2ff375aa268c39e63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426949"
---
# <span data-ttu-id="60b71-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="60b71-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="60b71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60b71-102">SYNOPSIS</span></span>
<span data-ttu-id="60b71-103">Revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="60b71-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60b71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60b71-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60b71-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60b71-105">DESCRIPTION</span></span>
<span data-ttu-id="60b71-106">O cmdlet **REVOKE-AzureRmDiskAccess** revoga um acesso a um disco.</span><span class="sxs-lookup"><span data-stu-id="60b71-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="60b71-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60b71-107">EXAMPLES</span></span>

### <span data-ttu-id="60b71-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="60b71-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="60b71-109">Revogue o acesso ao disco chamado ' Disk01 ' no grupo de recursos chamado ' ResourceGroup01 '</span><span class="sxs-lookup"><span data-stu-id="60b71-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="60b71-110">OS</span><span class="sxs-lookup"><span data-stu-id="60b71-110">PARAMETERS</span></span>

### <span data-ttu-id="60b71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b71-111">-DefaultProfile</span></span>
<span data-ttu-id="60b71-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60b71-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60b71-113">-Diskname</span><span class="sxs-lookup"><span data-stu-id="60b71-113">-DiskName</span></span>
<span data-ttu-id="60b71-114">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="60b71-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="60b71-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60b71-115">-ResourceGroupName</span></span>
<span data-ttu-id="60b71-116">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60b71-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="60b71-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60b71-117">-Confirm</span></span>
<span data-ttu-id="60b71-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60b71-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60b71-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60b71-119">-WhatIf</span></span>
<span data-ttu-id="60b71-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60b71-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60b71-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60b71-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60b71-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b71-122">CommonParameters</span></span>
<span data-ttu-id="60b71-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60b71-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b71-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60b71-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b71-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60b71-125">INPUTS</span></span>

### <span data-ttu-id="60b71-126">System. String</span><span class="sxs-lookup"><span data-stu-id="60b71-126">System.String</span></span>

## <span data-ttu-id="60b71-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60b71-127">OUTPUTS</span></span>

### <span data-ttu-id="60b71-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="60b71-128">System.Object</span></span>

## <span data-ttu-id="60b71-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60b71-129">NOTES</span></span>

## <span data-ttu-id="60b71-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60b71-130">RELATED LINKS</span></span>

