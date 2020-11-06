---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 05a4b2a475b2bd58de706ba038f2760d133b7dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431301"
---
# <span data-ttu-id="d024c-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="d024c-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="d024c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d024c-102">SYNOPSIS</span></span>
<span data-ttu-id="d024c-103">Remove pontos de extremidade e metadados para se conectar a uma determinada instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="d024c-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d024c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d024c-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d024c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d024c-105">DESCRIPTION</span></span>
<span data-ttu-id="d024c-106">O cmdlet Remove-AzureRmEnvironment remove pontos de extremidade e informações de metadados para se conectar a uma determinada instância do Azure.</span><span class="sxs-lookup"><span data-stu-id="d024c-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="d024c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d024c-107">EXAMPLES</span></span>

### <span data-ttu-id="d024c-108">Exemplo 1: Criando e removendo um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="d024c-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="d024c-109">Este exemplo mostra como criar um ambiente usando Add-AzureRmEnvironment e, em seguida, como excluir o ambiente usando Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="d024c-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="d024c-110">OS</span><span class="sxs-lookup"><span data-stu-id="d024c-110">PARAMETERS</span></span>

### <span data-ttu-id="d024c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d024c-111">-DefaultProfile</span></span>
<span data-ttu-id="d024c-112">As credenciais, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d024c-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d024c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d024c-113">-Name</span></span>
<span data-ttu-id="d024c-114">Especifica o nome do ambiente a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d024c-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="d024c-115">-Escopo</span><span class="sxs-lookup"><span data-stu-id="d024c-115">-Scope</span></span>
<span data-ttu-id="d024c-116">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="d024c-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="d024c-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d024c-117">-Confirm</span></span>
<span data-ttu-id="d024c-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d024c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d024c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d024c-119">-WhatIf</span></span>
<span data-ttu-id="d024c-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d024c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d024c-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d024c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d024c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d024c-122">CommonParameters</span></span>
<span data-ttu-id="d024c-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d024c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d024c-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d024c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d024c-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d024c-125">INPUTS</span></span>

### <span data-ttu-id="d024c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d024c-126">System.String</span></span>

## <span data-ttu-id="d024c-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d024c-127">OUTPUTS</span></span>

### <span data-ttu-id="d024c-128">Microsoft. Azure. Commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d024c-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="d024c-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d024c-129">NOTES</span></span>

## <span data-ttu-id="d024c-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d024c-130">RELATED LINKS</span></span>

[<span data-ttu-id="d024c-131">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="d024c-131">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="d024c-132">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="d024c-132">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="d024c-133">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="d024c-133">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

