---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: aa1bfb0760480d5c2e24e113653037ecb83a9f6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901378"
---
# <span data-ttu-id="5a380-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="5a380-101">Get-AzDefault</span></span>

## <span data-ttu-id="5a380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a380-102">SYNOPSIS</span></span>
<span data-ttu-id="5a380-103">Obter os padrões definidos pelo usuário no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="5a380-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="5a380-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5a380-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a380-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5a380-105">DESCRIPTION</span></span>
<span data-ttu-id="5a380-106">O Get-AzDefault cmdlet obtém o Grupo de Recursos que o usuário definiu como padrão no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="5a380-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="5a380-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a380-107">EXAMPLES</span></span>

### <span data-ttu-id="5a380-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5a380-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="5a380-109">Este comando retorna os padrões atuais se houver padrões definidos ou retorna nada se nenhum padrão for definido.</span><span class="sxs-lookup"><span data-stu-id="5a380-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="5a380-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5a380-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="5a380-111">Este comando retornará o Grupo de Recursos padrão atual se houver um conjunto padrão ou retornará nada se nenhum padrão for definido.</span><span class="sxs-lookup"><span data-stu-id="5a380-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="5a380-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5a380-112">PARAMETERS</span></span>

### <span data-ttu-id="5a380-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a380-113">-DefaultProfile</span></span>
<span data-ttu-id="5a380-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5a380-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a380-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5a380-115">-ResourceGroup</span></span>
<span data-ttu-id="5a380-116">Exibir Grupo de Recursos Padrão</span><span class="sxs-lookup"><span data-stu-id="5a380-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="5a380-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a380-117">CommonParameters</span></span>
<span data-ttu-id="5a380-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a380-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a380-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a380-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a380-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a380-120">INPUTS</span></span>

### <span data-ttu-id="5a380-121">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5a380-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a380-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5a380-122">OUTPUTS</span></span>

### <span data-ttu-id="5a380-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5a380-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="5a380-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="5a380-124">NOTES</span></span>

## <span data-ttu-id="5a380-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a380-125">RELATED LINKS</span></span>
