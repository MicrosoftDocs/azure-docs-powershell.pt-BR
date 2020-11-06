---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: c5276ddbcd10870355f8530c2f04f81122dda382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602695"
---
# <span data-ttu-id="4603b-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4603b-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="4603b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4603b-102">SYNOPSIS</span></span>
<span data-ttu-id="4603b-103">Lista os aplicativos existentes do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4603b-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4603b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4603b-104">SYNTAX</span></span>

### <span data-ttu-id="4603b-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4603b-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4603b-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4603b-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4603b-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4603b-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4603b-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4603b-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4603b-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="4603b-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4603b-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4603b-110">DESCRIPTION</span></span>
<span data-ttu-id="4603b-111">Lista os aplicativos existentes do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4603b-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="4603b-112">A pesquisa do aplicativo pode ser feita por ObjectId, ApplicationId, IdentifierUri ou DisplayName.</span><span class="sxs-lookup"><span data-stu-id="4603b-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="4603b-113">Se nenhum parâmetro for fornecido, ele buscará todos os aplicativos sob o locatário.</span><span class="sxs-lookup"><span data-stu-id="4603b-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="4603b-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4603b-114">EXAMPLES</span></span>

### <span data-ttu-id="4603b-115">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4603b-115">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="4603b-116">Lista todos os aplicativos em um locatário.</span><span class="sxs-lookup"><span data-stu-id="4603b-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="4603b-117">--------------------------Exemplo 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4603b-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="4603b-118">Obtém o aplicativo com URI de identificador como " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="4603b-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="4603b-119">OS</span><span class="sxs-lookup"><span data-stu-id="4603b-119">PARAMETERS</span></span>

### <span data-ttu-id="4603b-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4603b-120">-ApplicationId</span></span>
<span data-ttu-id="4603b-121">A ID do aplicativo do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="4603b-121">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4603b-122">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="4603b-122">-DisplayNameStartWith</span></span>
<span data-ttu-id="4603b-123">Busque todos os aplicativos que começam com o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="4603b-123">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4603b-124">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="4603b-124">-IdentifierUri</span></span>
<span data-ttu-id="4603b-125">URI do identificador exclusivo do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="4603b-125">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4603b-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4603b-126">-ObjectId</span></span>
<span data-ttu-id="4603b-127">A ID do objeto do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="4603b-127">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4603b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4603b-128">-DefaultProfile</span></span>
<span data-ttu-id="4603b-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4603b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4603b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4603b-130">CommonParameters</span></span>
<span data-ttu-id="4603b-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4603b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4603b-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4603b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4603b-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4603b-133">INPUTS</span></span>

## <span data-ttu-id="4603b-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4603b-134">OUTPUTS</span></span>

### <span data-ttu-id="4603b-135">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="4603b-135">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="4603b-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4603b-136">NOTES</span></span>

## <span data-ttu-id="4603b-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4603b-137">RELATED LINKS</span></span>

[<span data-ttu-id="4603b-138">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4603b-138">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="4603b-139">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4603b-139">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="4603b-140">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4603b-140">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="4603b-141">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4603b-141">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="4603b-142">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4603b-142">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="4603b-143">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4603b-143">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

