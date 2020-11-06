---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 67af78e767b8da7764053e3652e25aef53f2877e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432550"
---
# <span data-ttu-id="14090-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="14090-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="14090-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14090-102">SYNOPSIS</span></span>
<span data-ttu-id="14090-103">Atualiza uma entidade de serviço existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="14090-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14090-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14090-104">SYNTAX</span></span>

### <span data-ttu-id="14090-105">SpObjectIdWithDisplayNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="14090-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14090-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14090-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14090-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14090-107">DESCRIPTION</span></span>
<span data-ttu-id="14090-108">Atualiza uma entidade de serviço existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="14090-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="14090-109">Para atualizar as credenciais associadas a essa entidade de serviço, use o cmdlet New-AzureRmADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="14090-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="14090-110">Para atualizar as propriedades associadas ao aplicativo subjacente, use Set-AzureRmADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14090-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="14090-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14090-111">EXAMPLES</span></span>

### <span data-ttu-id="14090-112">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="14090-112">--------------------------  Example 1  --------------------------</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="14090-113">Atualiza o nome de exibição da entidade de serviço com a ID de objeto especificada.</span><span class="sxs-lookup"><span data-stu-id="14090-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="14090-114">--------------------------Exemplo 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="14090-114">--------------------------  Example 2  --------------------------</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="14090-115">Atualiza o nome de exibição para a entidade de serviço com o nome de entidade de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="14090-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="14090-116">OS</span><span class="sxs-lookup"><span data-stu-id="14090-116">PARAMETERS</span></span>

### <span data-ttu-id="14090-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="14090-117">-DisplayName</span></span>
<span data-ttu-id="14090-118">Novo nome de exibição para a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="14090-118">New display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14090-119">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="14090-119">-ObjectId</span></span>
<span data-ttu-id="14090-120">A ID de objeto da entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="14090-120">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14090-121">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="14090-121">-ServicePrincipalName</span></span>
<span data-ttu-id="14090-122">O SPN da entidade de serviço a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="14090-122">The SPN of service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14090-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14090-123">-Confirm</span></span>
<span data-ttu-id="14090-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14090-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14090-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14090-125">-WhatIf</span></span>
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

### <span data-ttu-id="14090-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14090-126">-DefaultProfile</span></span>
<span data-ttu-id="14090-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14090-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14090-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14090-128">CommonParameters</span></span>
<span data-ttu-id="14090-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14090-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14090-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14090-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14090-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14090-131">INPUTS</span></span>

## <span data-ttu-id="14090-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14090-132">OUTPUTS</span></span>

## <span data-ttu-id="14090-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14090-133">NOTES</span></span>

## <span data-ttu-id="14090-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14090-134">RELATED LINKS</span></span>

[<span data-ttu-id="14090-135">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="14090-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="14090-136">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="14090-136">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="14090-137">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="14090-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="14090-138">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="14090-138">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="14090-139">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="14090-139">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="14090-140">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="14090-140">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

