---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 853404bce6d45f2824c574b249c434ccebc281ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433430"
---
# <span data-ttu-id="c82f9-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c82f9-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="c82f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c82f9-102">SYNOPSIS</span></span>
<span data-ttu-id="c82f9-103">Atualiza uma entidade de serviço existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c82f9-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c82f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c82f9-104">SYNTAX</span></span>

### <span data-ttu-id="c82f9-105">SpObjectIdWithDisplayNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c82f9-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c82f9-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c82f9-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c82f9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c82f9-107">DESCRIPTION</span></span>
<span data-ttu-id="c82f9-108">Atualiza uma entidade de serviço existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c82f9-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="c82f9-109">Para atualizar as credenciais associadas a essa entidade de serviço, use o cmdlet New-AzureRmADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="c82f9-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="c82f9-110">Para atualizar as propriedades associadas ao aplicativo subjacente, use Set-AzureRmADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c82f9-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="c82f9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c82f9-111">EXAMPLES</span></span>

### <span data-ttu-id="c82f9-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c82f9-112">Example 1</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="c82f9-113">Atualiza o nome de exibição da entidade de serviço com a ID de objeto especificada.</span><span class="sxs-lookup"><span data-stu-id="c82f9-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="c82f9-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c82f9-114">Example 2</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="c82f9-115">Atualiza o nome de exibição para a entidade de serviço com o nome de entidade de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="c82f9-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="c82f9-116">OS</span><span class="sxs-lookup"><span data-stu-id="c82f9-116">PARAMETERS</span></span>

### <span data-ttu-id="c82f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c82f9-117">-DefaultProfile</span></span>
<span data-ttu-id="c82f9-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c82f9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c82f9-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c82f9-119">-DisplayName</span></span>
<span data-ttu-id="c82f9-120">Novo nome de exibição para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="c82f9-120">New display name for the service principal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c82f9-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c82f9-121">-ObjectId</span></span>
<span data-ttu-id="c82f9-122">A ID de objeto da entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="c82f9-122">The object id of the service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c82f9-123">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="c82f9-123">-ServicePrincipalName</span></span>
<span data-ttu-id="c82f9-124">O SPN da entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="c82f9-124">The SPN of service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c82f9-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c82f9-125">-Confirm</span></span>
<span data-ttu-id="c82f9-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c82f9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c82f9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c82f9-127">-WhatIf</span></span>
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

### <span data-ttu-id="c82f9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c82f9-128">CommonParameters</span></span>
<span data-ttu-id="c82f9-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c82f9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c82f9-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c82f9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c82f9-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c82f9-131">INPUTS</span></span>

### <span data-ttu-id="c82f9-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c82f9-132">None</span></span>
<span data-ttu-id="c82f9-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c82f9-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c82f9-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c82f9-134">OUTPUTS</span></span>

## <span data-ttu-id="c82f9-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c82f9-135">NOTES</span></span>

## <span data-ttu-id="c82f9-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c82f9-136">RELATED LINKS</span></span>

[<span data-ttu-id="c82f9-137">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c82f9-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="c82f9-138">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c82f9-138">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="c82f9-139">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c82f9-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="c82f9-140">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c82f9-140">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="c82f9-141">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c82f9-141">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="c82f9-142">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c82f9-142">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

