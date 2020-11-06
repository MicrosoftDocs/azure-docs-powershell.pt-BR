---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 1079486422da769863e86d3fc16d1c3ec65d6f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429126"
---
# <span data-ttu-id="b3ff3-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="b3ff3-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="b3ff3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ff3-103">Filtra grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b3ff3-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3ff3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3ff3-104">SYNTAX</span></span>

### <span data-ttu-id="b3ff3-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b3ff3-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3ff3-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3ff3-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3ff3-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3ff3-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3ff3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3ff3-108">DESCRIPTION</span></span>
<span data-ttu-id="b3ff3-109">Filtra grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b3ff3-109">Filters active directory groups.</span></span>

## <span data-ttu-id="b3ff3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3ff3-110">EXAMPLES</span></span>

### <span data-ttu-id="b3ff3-111">--------------------------Grupos de filtros usando a ID de objeto--------------------------</span><span class="sxs-lookup"><span data-stu-id="b3ff3-111">--------------------------  Filters groups using object id  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="b3ff3-112">Obtém o grupo com a ID 85F89C90-780E-4AA6-9F4F-6F268D322EEE</span><span class="sxs-lookup"><span data-stu-id="b3ff3-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="b3ff3-113">--------------------------Grupos de filtros usando a cadeia de caracteres de pesquisa--------------------------</span><span class="sxs-lookup"><span data-stu-id="b3ff3-113">--------------------------  Filters groups using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="b3ff3-114">Filtra todos os grupos de anúncios que têm Joe no nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="b3ff3-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="b3ff3-115">--------------------------Lista de grupos de anúncios--------------------------</span><span class="sxs-lookup"><span data-stu-id="b3ff3-115">--------------------------  List AD groups  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="b3ff3-116">Obtém todos os grupos de anúncios</span><span class="sxs-lookup"><span data-stu-id="b3ff3-116">Gets all AD groups</span></span>

## <span data-ttu-id="b3ff3-117">OS</span><span class="sxs-lookup"><span data-stu-id="b3ff3-117">PARAMETERS</span></span>

### <span data-ttu-id="b3ff3-118">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b3ff3-118">-ObjectId</span></span>
<span data-ttu-id="b3ff3-119">ID de objeto do grupo.</span><span class="sxs-lookup"><span data-stu-id="b3ff3-119">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="b3ff3-120">-Searchstring</span><span class="sxs-lookup"><span data-stu-id="b3ff3-120">-SearchString</span></span>
<span data-ttu-id="b3ff3-121">O nome de exibição do grupo</span><span class="sxs-lookup"><span data-stu-id="b3ff3-121">The group display name</span></span>

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

### <span data-ttu-id="b3ff3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ff3-122">-DefaultProfile</span></span>
<span data-ttu-id="b3ff3-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3ff3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3ff3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ff3-124">CommonParameters</span></span>
<span data-ttu-id="b3ff3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3ff3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ff3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3ff3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ff3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3ff3-127">INPUTS</span></span>

## <span data-ttu-id="b3ff3-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3ff3-128">OUTPUTS</span></span>

### <span data-ttu-id="b3ff3-129">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup]</span><span class="sxs-lookup"><span data-stu-id="b3ff3-129">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="b3ff3-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3ff3-130">NOTES</span></span>

## <span data-ttu-id="b3ff3-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3ff3-131">RELATED LINKS</span></span>

[<span data-ttu-id="b3ff3-132">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b3ff3-132">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="b3ff3-133">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b3ff3-133">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b3ff3-134">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="b3ff3-134">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

