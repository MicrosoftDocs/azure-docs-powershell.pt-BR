---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 2c7ba44358db4e6a578f9876e26a099b2242badc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114324"
---
# <span data-ttu-id="e0f83-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0f83-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="e0f83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0f83-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f83-103">Remove pontos de extremidade e metadados para se conectar a uma determinada instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f83-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="e0f83-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0f83-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0f83-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0f83-105">DESCRIPTION</span></span>
<span data-ttu-id="e0f83-106">O Remove-AzEnvironment cmdlet remove pontos de extremidade e informações de metadados para se conectar a uma determinada instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f83-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="e0f83-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0f83-107">EXAMPLES</span></span>

### <span data-ttu-id="e0f83-108">Exemplo 1: Criar e remover um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="e0f83-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="e0f83-109">Este exemplo mostra como criar um ambiente usando o Add-AzEnvironment e como excluir o ambiente usando Remove-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="e0f83-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="e0f83-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0f83-110">PARAMETERS</span></span>

### <span data-ttu-id="e0f83-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f83-111">-DefaultProfile</span></span>
<span data-ttu-id="e0f83-112">As credenciais, locatário e assinatura usados para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e0f83-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0f83-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0f83-113">-Name</span></span>
<span data-ttu-id="e0f83-114">Especifica o nome do ambiente a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e0f83-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="e0f83-115">-Escopo</span><span class="sxs-lookup"><span data-stu-id="e0f83-115">-Scope</span></span>
<span data-ttu-id="e0f83-116">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="e0f83-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="e0f83-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e0f83-117">-Confirm</span></span>
<span data-ttu-id="e0f83-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0f83-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0f83-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0f83-119">-WhatIf</span></span>
<span data-ttu-id="e0f83-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e0f83-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0f83-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0f83-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0f83-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f83-122">CommonParameters</span></span>
<span data-ttu-id="e0f83-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0f83-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f83-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0f83-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f83-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="e0f83-125">INPUTS</span></span>

### <span data-ttu-id="e0f83-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e0f83-126">System.String</span></span>

## <span data-ttu-id="e0f83-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="e0f83-127">OUTPUTS</span></span>

### <span data-ttu-id="e0f83-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0f83-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="e0f83-129">Notas</span><span class="sxs-lookup"><span data-stu-id="e0f83-129">NOTES</span></span>

## <span data-ttu-id="e0f83-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0f83-130">RELATED LINKS</span></span>

[<span data-ttu-id="e0f83-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0f83-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="e0f83-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0f83-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="e0f83-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e0f83-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

