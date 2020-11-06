---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: dd864d11608c33f758e0995d9dacf4afc454130a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427800"
---
# <span data-ttu-id="9bd21-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="9bd21-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="9bd21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bd21-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd21-103">Filtra usuários do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9bd21-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bd21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bd21-104">SYNTAX</span></span>

### <span data-ttu-id="9bd21-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9bd21-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bd21-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd21-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bd21-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd21-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bd21-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd21-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bd21-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd21-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bd21-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9bd21-110">DESCRIPTION</span></span>
<span data-ttu-id="9bd21-111">Filtra usuários do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9bd21-111">Filters active directory users.</span></span>

## <span data-ttu-id="9bd21-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bd21-112">EXAMPLES</span></span>

### <span data-ttu-id="9bd21-113">--------------------------Filtra usuários que usam--------------------------UPN</span><span class="sxs-lookup"><span data-stu-id="9bd21-113">--------------------------  Filters users using UPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="9bd21-114">Obtém o usuário foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="9bd21-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="9bd21-115">--------------------------Filtra os usuários usando a cadeia de caracteres de pesquisa--------------------------</span><span class="sxs-lookup"><span data-stu-id="9bd21-115">--------------------------  Filters users using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="9bd21-116">Filtra todos os usuários do AD que têm Joe no nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="9bd21-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="9bd21-117">--------------------------Lista--------------------------usuários do AD</span><span class="sxs-lookup"><span data-stu-id="9bd21-117">--------------------------  List AD users  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="9bd21-118">Obtém todos os usuários do AD</span><span class="sxs-lookup"><span data-stu-id="9bd21-118">Gets all AD users</span></span>

## <span data-ttu-id="9bd21-119">OS</span><span class="sxs-lookup"><span data-stu-id="9bd21-119">PARAMETERS</span></span>

### <span data-ttu-id="9bd21-120">-Mail</span><span class="sxs-lookup"><span data-stu-id="9bd21-120">-Mail</span></span>
```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd21-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9bd21-121">-ObjectId</span></span>
<span data-ttu-id="9bd21-122">ID do objeto do usuário.</span><span class="sxs-lookup"><span data-stu-id="9bd21-122">Object id of the user.</span></span>

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

### <span data-ttu-id="9bd21-123">-Searchstring</span><span class="sxs-lookup"><span data-stu-id="9bd21-123">-SearchString</span></span>
<span data-ttu-id="9bd21-124">O nome de exibição do usuário</span><span class="sxs-lookup"><span data-stu-id="9bd21-124">The user display name</span></span>

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

### <span data-ttu-id="9bd21-125">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9bd21-125">-UserPrincipalName</span></span>
<span data-ttu-id="9bd21-126">UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="9bd21-126">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd21-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd21-127">-DefaultProfile</span></span>
<span data-ttu-id="9bd21-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd21-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bd21-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd21-129">CommonParameters</span></span>
<span data-ttu-id="9bd21-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd21-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd21-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd21-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd21-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9bd21-132">INPUTS</span></span>

## <span data-ttu-id="9bd21-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9bd21-133">OUTPUTS</span></span>

### <span data-ttu-id="9bd21-134">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="9bd21-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="9bd21-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9bd21-135">NOTES</span></span>

## <span data-ttu-id="9bd21-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bd21-136">RELATED LINKS</span></span>

[<span data-ttu-id="9bd21-137">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="9bd21-137">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="9bd21-138">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="9bd21-138">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="9bd21-139">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="9bd21-139">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

