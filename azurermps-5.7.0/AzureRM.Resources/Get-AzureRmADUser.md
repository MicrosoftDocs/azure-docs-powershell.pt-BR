---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: e111da68e00e0edad54823c763c06f84ea5100e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603236"
---
# <span data-ttu-id="9a976-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="9a976-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="9a976-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a976-102">SYNOPSIS</span></span>
<span data-ttu-id="9a976-103">Filtra usuários do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9a976-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a976-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a976-104">SYNTAX</span></span>

### <span data-ttu-id="9a976-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9a976-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a976-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a976-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a976-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a976-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a976-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a976-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a976-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a976-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a976-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a976-110">DESCRIPTION</span></span>
<span data-ttu-id="9a976-111">Filtra usuários do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9a976-111">Filters active directory users.</span></span>

## <span data-ttu-id="9a976-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a976-112">EXAMPLES</span></span>

### <span data-ttu-id="9a976-113">Filtra usuários usando o UPN</span><span class="sxs-lookup"><span data-stu-id="9a976-113">Filters users using UPN</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="9a976-114">Obtém o usuário foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="9a976-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="9a976-115">Filtra usuários usando a cadeia de pesquisa</span><span class="sxs-lookup"><span data-stu-id="9a976-115">Filters users using Search String</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="9a976-116">Filtra todos os usuários do AD que têm Joe no nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="9a976-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="9a976-117">Listar usuários de anúncios</span><span class="sxs-lookup"><span data-stu-id="9a976-117">List AD users</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="9a976-118">Obtém todos os usuários do AD</span><span class="sxs-lookup"><span data-stu-id="9a976-118">Gets all AD users</span></span>

## <span data-ttu-id="9a976-119">OS</span><span class="sxs-lookup"><span data-stu-id="9a976-119">PARAMETERS</span></span>

### <span data-ttu-id="9a976-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a976-120">-DefaultProfile</span></span>
<span data-ttu-id="9a976-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9a976-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a976-122">-Mail</span><span class="sxs-lookup"><span data-stu-id="9a976-122">-Mail</span></span>
```yaml
Type: String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a976-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9a976-123">-ObjectId</span></span>
<span data-ttu-id="9a976-124">ID do objeto do usuário.</span><span class="sxs-lookup"><span data-stu-id="9a976-124">Object id of the user.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a976-125">-Searchstring</span><span class="sxs-lookup"><span data-stu-id="9a976-125">-SearchString</span></span>
<span data-ttu-id="9a976-126">O nome de exibição do usuário</span><span class="sxs-lookup"><span data-stu-id="9a976-126">The user display name</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a976-127">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9a976-127">-UserPrincipalName</span></span>
<span data-ttu-id="9a976-128">UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="9a976-128">UPN of the user.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a976-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a976-129">CommonParameters</span></span>
<span data-ttu-id="9a976-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a976-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a976-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a976-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a976-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a976-132">INPUTS</span></span>

### <span data-ttu-id="9a976-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9a976-133">None</span></span>
<span data-ttu-id="9a976-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9a976-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a976-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a976-135">OUTPUTS</span></span>

### <span data-ttu-id="9a976-136">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="9a976-136">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="9a976-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a976-137">NOTES</span></span>

## <span data-ttu-id="9a976-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a976-138">RELATED LINKS</span></span>

[<span data-ttu-id="9a976-139">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="9a976-139">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="9a976-140">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="9a976-140">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="9a976-141">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="9a976-141">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

