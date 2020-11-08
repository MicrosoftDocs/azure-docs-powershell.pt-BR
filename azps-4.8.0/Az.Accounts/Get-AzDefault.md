---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 43806326f572030997299353cfc7e79e5587a4ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111919"
---
# <span data-ttu-id="9fa57-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="9fa57-101">Get-AzDefault</span></span>

## <span data-ttu-id="9fa57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fa57-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa57-103">Obter os padrões definidos pelo usuário no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="9fa57-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="9fa57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fa57-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fa57-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fa57-105">DESCRIPTION</span></span>
<span data-ttu-id="9fa57-106">O cmdlet Get-AzDefault Obtém o grupo de recursos que o usuário definiu como padrão no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="9fa57-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="9fa57-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fa57-107">EXAMPLES</span></span>

### <span data-ttu-id="9fa57-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9fa57-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="9fa57-109">Esse comando retorna os padrões atuais se houver padrões definidos ou retorna nada se nenhum padrão for definido.</span><span class="sxs-lookup"><span data-stu-id="9fa57-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="9fa57-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9fa57-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="9fa57-111">Esse comando retorna o grupo de recursos padrão atual se houver um conjunto padrão ou retornará nada se nenhum padrão for definido.</span><span class="sxs-lookup"><span data-stu-id="9fa57-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="9fa57-112">OS</span><span class="sxs-lookup"><span data-stu-id="9fa57-112">PARAMETERS</span></span>

### <span data-ttu-id="9fa57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa57-113">-DefaultProfile</span></span>
<span data-ttu-id="9fa57-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa57-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fa57-115">-Resource</span><span class="sxs-lookup"><span data-stu-id="9fa57-115">-ResourceGroup</span></span>
<span data-ttu-id="9fa57-116">Exibir grupo de recursos padrão</span><span class="sxs-lookup"><span data-stu-id="9fa57-116">Display Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa57-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa57-117">CommonParameters</span></span>
<span data-ttu-id="9fa57-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa57-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa57-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa57-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa57-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fa57-120">INPUTS</span></span>

### <span data-ttu-id="9fa57-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9fa57-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9fa57-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fa57-122">OUTPUTS</span></span>

### <span data-ttu-id="9fa57-123">Microsoft. Azure. Commands. Profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9fa57-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="9fa57-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fa57-124">NOTES</span></span>

## <span data-ttu-id="9fa57-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fa57-125">RELATED LINKS</span></span>
