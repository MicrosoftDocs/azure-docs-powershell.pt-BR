---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 34f4b85a299e714f524b1a4d33f2fb717483c377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440563"
---
# <span data-ttu-id="d0b6d-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0b6d-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="d0b6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b6d-103">Filtra as entidades de serviço do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0b6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0b6d-104">SYNTAX</span></span>

### <span data-ttu-id="d0b6d-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d0b6d-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0b6d-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0b6d-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0b6d-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0b6d-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0b6d-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0b6d-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0b6d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0b6d-109">DESCRIPTION</span></span>
<span data-ttu-id="d0b6d-110">Filtra as entidades de serviço do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="d0b6d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0b6d-111">EXAMPLES</span></span>

### <span data-ttu-id="d0b6d-112">Entidades de serviço de filtros--------------------------usando SPN--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0b6d-112">--------------------------  Filters service principals using SPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="d0b6d-113">Obtém as entidades de serviço com o SPN do 36f81fc3-b00f-48CD-8218-3879f51ff39f.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="d0b6d-114">Entidades de serviço de filtros--------------------------usando a cadeia de caracteres de pesquisa--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0b6d-114">--------------------------  Filters service principals using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="d0b6d-115">Filtra todas as entidades de serviço de anúncio que têm o nome de exibição começando com "Web".</span><span class="sxs-lookup"><span data-stu-id="d0b6d-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="d0b6d-116">--------------------------Principais de serviço de anúncios de lista--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0b6d-116">--------------------------  List AD service principals  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="d0b6d-117">Obtém todas as entidades de serviço de anúncios.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="d0b6d-118">OS</span><span class="sxs-lookup"><span data-stu-id="d0b6d-118">PARAMETERS</span></span>

### <span data-ttu-id="d0b6d-119">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d0b6d-119">-ObjectId</span></span>
<span data-ttu-id="d0b6d-120">ID de objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-120">Object id of the service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b6d-121">-Searchstring</span><span class="sxs-lookup"><span data-stu-id="d0b6d-121">-SearchString</span></span>
<span data-ttu-id="d0b6d-122">Busca todas as entidades de serviço que tenham o nome de exibição começando com esse valor.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-122">Fetches all service principals that have the display name starting with this value.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b6d-123">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="d0b6d-123">-ServicePrincipalName</span></span>
<span data-ttu-id="d0b6d-124">SPN do serviço.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-124">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: SPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b6d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b6d-125">-DefaultProfile</span></span>
<span data-ttu-id="d0b6d-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0b6d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b6d-127">CommonParameters</span></span>
<span data-ttu-id="d0b6d-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0b6d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b6d-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0b6d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b6d-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0b6d-130">INPUTS</span></span>

## <span data-ttu-id="d0b6d-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0b6d-131">OUTPUTS</span></span>

### <span data-ttu-id="d0b6d-132">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="d0b6d-132">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="d0b6d-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0b6d-133">NOTES</span></span>

## <span data-ttu-id="d0b6d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0b6d-134">RELATED LINKS</span></span>

[<span data-ttu-id="d0b6d-135">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0b6d-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="d0b6d-136">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0b6d-136">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="d0b6d-137">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0b6d-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="d0b6d-138">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d0b6d-138">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="d0b6d-139">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d0b6d-139">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

