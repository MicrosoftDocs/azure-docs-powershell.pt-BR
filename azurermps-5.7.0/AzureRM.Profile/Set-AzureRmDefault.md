---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
ms.openlocfilehash: 01b8283277c1d9592adbd8edfe6b883a4451ded9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603249"
---
# <span data-ttu-id="0f2f0-101">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="0f2f0-101">Set-AzureRmDefault</span></span>

## <span data-ttu-id="0f2f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f2f0-102">SYNOPSIS</span></span>
<span data-ttu-id="0f2f0-103">Define um padrão no contexto atual</span><span class="sxs-lookup"><span data-stu-id="0f2f0-103">Sets a default in the current context</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f2f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f2f0-104">SYNTAX</span></span>

```
Set-AzureRmDefault [-ResourceGroupName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f2f0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f2f0-105">DESCRIPTION</span></span>
<span data-ttu-id="0f2f0-106">O cmdlet Set-AzureRmDefault adiciona ou altera os padrões no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="0f2f0-106">The Set-AzureRmDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="0f2f0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f2f0-107">EXAMPLES</span></span>

### <span data-ttu-id="0f2f0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f2f0-108">Example 1</span></span>
```
PS C:\> Set-AzureRmDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="0f2f0-109">Este comando define o grupo de recursos padrão para o grupo de recursos especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0f2f0-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="0f2f0-110">OS</span><span class="sxs-lookup"><span data-stu-id="0f2f0-110">PARAMETERS</span></span>

### <span data-ttu-id="0f2f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f2f0-111">-DefaultProfile</span></span>
<span data-ttu-id="0f2f0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f2f0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f2f0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0f2f0-113">-Force</span></span>
<span data-ttu-id="0f2f0-114">Criar um novo grupo de recursos se o padrão especificado não existir</span><span class="sxs-lookup"><span data-stu-id="0f2f0-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="0f2f0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f2f0-115">-ResourceGroupName</span></span>
<span data-ttu-id="0f2f0-116">Nome do grupo de recursos sendo definido como padrão</span><span class="sxs-lookup"><span data-stu-id="0f2f0-116">Name of the resource group being set as default</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2f0-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0f2f0-117">-Confirm</span></span>
<span data-ttu-id="0f2f0-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f2f0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f2f0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f2f0-119">-WhatIf</span></span>
<span data-ttu-id="0f2f0-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f2f0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f2f0-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f2f0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f2f0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f2f0-122">CommonParameters</span></span>
<span data-ttu-id="0f2f0-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f2f0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f2f0-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f2f0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f2f0-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f2f0-125">INPUTS</span></span>

### <span data-ttu-id="0f2f0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0f2f0-126">System.String</span></span>

## <span data-ttu-id="0f2f0-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f2f0-127">OUTPUTS</span></span>

### <span data-ttu-id="0f2f0-128">Microsoft. Azure. Management. Internal. Resources. Models. resourcement</span><span class="sxs-lookup"><span data-stu-id="0f2f0-128">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="0f2f0-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f2f0-129">NOTES</span></span>

## <span data-ttu-id="0f2f0-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f2f0-130">RELATED LINKS</span></span>

