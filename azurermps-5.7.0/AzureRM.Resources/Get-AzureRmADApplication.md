---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: b44d3bbf7c594f5f9114488b536d28fd17fe56c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432915"
---
# <span data-ttu-id="67990-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="67990-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="67990-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67990-102">SYNOPSIS</span></span>
<span data-ttu-id="67990-103">Lista os aplicativos existentes do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="67990-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67990-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67990-104">SYNTAX</span></span>

### <span data-ttu-id="67990-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="67990-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67990-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67990-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67990-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67990-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67990-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="67990-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67990-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="67990-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67990-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67990-110">DESCRIPTION</span></span>
<span data-ttu-id="67990-111">Lista os aplicativos existentes do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="67990-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="67990-112">A pesquisa do aplicativo pode ser feita por ObjectId, ApplicationId, IdentifierUri ou DisplayName.</span><span class="sxs-lookup"><span data-stu-id="67990-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="67990-113">Se nenhum parâmetro for fornecido, ele buscará todos os aplicativos sob o locatário.</span><span class="sxs-lookup"><span data-stu-id="67990-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="67990-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67990-114">EXAMPLES</span></span>

### <span data-ttu-id="67990-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67990-115">Example 1</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="67990-116">Lista todos os aplicativos em um locatário.</span><span class="sxs-lookup"><span data-stu-id="67990-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="67990-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="67990-117">Example 2</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="67990-118">Obtém o aplicativo com URI de identificador como " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="67990-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="67990-119">OS</span><span class="sxs-lookup"><span data-stu-id="67990-119">PARAMETERS</span></span>

### <span data-ttu-id="67990-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="67990-120">-ApplicationId</span></span>
<span data-ttu-id="67990-121">A ID do aplicativo do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="67990-121">The application id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67990-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67990-122">-DefaultProfile</span></span>
<span data-ttu-id="67990-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="67990-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67990-124">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="67990-124">-DisplayNameStartWith</span></span>
<span data-ttu-id="67990-125">Busque todos os aplicativos que começam com o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="67990-125">Fetch all applications starting with the display name.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67990-126">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="67990-126">-IdentifierUri</span></span>
<span data-ttu-id="67990-127">URI do identificador exclusivo do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="67990-127">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67990-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="67990-128">-ObjectId</span></span>
<span data-ttu-id="67990-129">A ID do objeto do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="67990-129">The object id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67990-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67990-130">CommonParameters</span></span>
<span data-ttu-id="67990-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67990-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67990-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67990-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67990-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67990-133">INPUTS</span></span>

### <span data-ttu-id="67990-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="67990-134">None</span></span>
<span data-ttu-id="67990-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="67990-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67990-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67990-136">OUTPUTS</span></span>

### <span data-ttu-id="67990-137">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="67990-137">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="67990-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67990-138">NOTES</span></span>

## <span data-ttu-id="67990-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67990-139">RELATED LINKS</span></span>

[<span data-ttu-id="67990-140">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="67990-140">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="67990-141">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="67990-141">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="67990-142">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="67990-142">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="67990-143">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="67990-143">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="67990-144">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="67990-144">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="67990-145">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="67990-145">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

