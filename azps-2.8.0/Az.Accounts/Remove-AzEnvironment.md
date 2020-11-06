---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 556b7fa95e005ff3622b64ba00d48df5e8c33339
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598241"
---
# <span data-ttu-id="b32ea-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b32ea-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="b32ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b32ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b32ea-103">Remove pontos de extremidade e metadados para se conectar a uma determinada instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="b32ea-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="b32ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b32ea-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b32ea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b32ea-105">DESCRIPTION</span></span>
<span data-ttu-id="b32ea-106">O cmdlet Remove-AzEnvironment remove pontos de extremidade e informações de metadados para se conectar a uma determinada instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="b32ea-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="b32ea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b32ea-107">EXAMPLES</span></span>

### <span data-ttu-id="b32ea-108">Exemplo 1: Criando e removendo um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="b32ea-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="b32ea-109">Este exemplo mostra como criar um ambiente usando Add-AzEnvironment e, em seguida, como excluir o ambiente usando Remove-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="b32ea-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="b32ea-110">OS</span><span class="sxs-lookup"><span data-stu-id="b32ea-110">PARAMETERS</span></span>

### <span data-ttu-id="b32ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32ea-111">-DefaultProfile</span></span>
<span data-ttu-id="b32ea-112">As credenciais, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b32ea-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b32ea-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b32ea-113">-Name</span></span>
<span data-ttu-id="b32ea-114">Especifica o nome do ambiente a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b32ea-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="b32ea-115">-Escopo</span><span class="sxs-lookup"><span data-stu-id="b32ea-115">-Scope</span></span>
<span data-ttu-id="b32ea-116">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="b32ea-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="b32ea-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b32ea-117">-Confirm</span></span>
<span data-ttu-id="b32ea-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b32ea-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b32ea-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b32ea-119">-WhatIf</span></span>
<span data-ttu-id="b32ea-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b32ea-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b32ea-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b32ea-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b32ea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32ea-122">CommonParameters</span></span>
<span data-ttu-id="b32ea-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b32ea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32ea-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b32ea-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32ea-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b32ea-125">INPUTS</span></span>

### <span data-ttu-id="b32ea-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b32ea-126">System.String</span></span>

## <span data-ttu-id="b32ea-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b32ea-127">OUTPUTS</span></span>

### <span data-ttu-id="b32ea-128">Microsoft. Azure. Commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="b32ea-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="b32ea-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b32ea-129">NOTES</span></span>

## <span data-ttu-id="b32ea-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b32ea-130">RELATED LINKS</span></span>

[<span data-ttu-id="b32ea-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b32ea-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="b32ea-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b32ea-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="b32ea-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b32ea-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

