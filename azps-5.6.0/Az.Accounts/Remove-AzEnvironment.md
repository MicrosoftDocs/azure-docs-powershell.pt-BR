---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 5acba21e8daf1adaa83820d67c5955b27230c4ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885750"
---
# <span data-ttu-id="4e3ec-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4e3ec-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="4e3ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4e3ec-103">Remove pontos de extremidade e metadados para se conectar a uma determinada instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e3ec-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="4e3ec-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4e3ec-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e3ec-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4e3ec-105">DESCRIPTION</span></span>
<span data-ttu-id="4e3ec-106">O Remove-AzEnvironment cmdlet remove pontos de extremidade e informações de metadados para se conectar a uma determinada instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e3ec-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="4e3ec-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e3ec-107">EXAMPLES</span></span>

### <span data-ttu-id="4e3ec-108">Exemplo 1: Criação e remoção de um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="4e3ec-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="4e3ec-109">Este exemplo mostra como criar um ambiente usando Add-AzEnvironment e como excluir o ambiente usando Remove-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="4e3ec-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="4e3ec-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4e3ec-110">PARAMETERS</span></span>

### <span data-ttu-id="4e3ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e3ec-111">-DefaultProfile</span></span>
<span data-ttu-id="4e3ec-112">As credenciais, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4e3ec-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e3ec-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4e3ec-113">-Name</span></span>
<span data-ttu-id="4e3ec-114">Especifica o nome do ambiente a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4e3ec-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="4e3ec-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="4e3ec-115">-Scope</span></span>
<span data-ttu-id="4e3ec-116">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="4e3ec-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e3ec-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e3ec-117">-Confirm</span></span>
<span data-ttu-id="4e3ec-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e3ec-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e3ec-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e3ec-119">-WhatIf</span></span>
<span data-ttu-id="4e3ec-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4e3ec-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e3ec-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4e3ec-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e3ec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e3ec-122">CommonParameters</span></span>
<span data-ttu-id="4e3ec-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e3ec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e3ec-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e3ec-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e3ec-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e3ec-125">INPUTS</span></span>

### <span data-ttu-id="4e3ec-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4e3ec-126">System.String</span></span>

## <span data-ttu-id="4e3ec-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4e3ec-127">OUTPUTS</span></span>

### <span data-ttu-id="4e3ec-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4e3ec-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="4e3ec-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="4e3ec-129">NOTES</span></span>

## <span data-ttu-id="4e3ec-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e3ec-130">RELATED LINKS</span></span>

[<span data-ttu-id="4e3ec-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4e3ec-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="4e3ec-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4e3ec-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="4e3ec-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4e3ec-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

