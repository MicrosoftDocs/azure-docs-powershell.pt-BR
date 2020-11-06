---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 8c03dd19fd2995347a3b4ae52de04fdcb3f02c30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602844"
---
# <span data-ttu-id="9462c-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9462c-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="9462c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9462c-102">SYNOPSIS</span></span>
<span data-ttu-id="9462c-103">Recupera uma lista de credenciais associadas a uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="9462c-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9462c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9462c-104">SYNTAX</span></span>

### <span data-ttu-id="9462c-105">ObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9462c-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9462c-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9462c-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9462c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9462c-107">DESCRIPTION</span></span>
<span data-ttu-id="9462c-108">O cmdlet Get-AzureRmADSpCredential pode ser usado para recuperar uma lista de credenciais associadas a uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="9462c-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="9462c-109">Esse comando recuperará todas as propriedades de credenciais (mas não o valor da credencial) associados à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="9462c-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="9462c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9462c-110">EXAMPLES</span></span>

### <span data-ttu-id="9462c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9462c-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="9462c-112">Retorna uma lista de credenciais associadas à entidade de serviço com SPN ' http://test12345 '.</span><span class="sxs-lookup"><span data-stu-id="9462c-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="9462c-113">OS</span><span class="sxs-lookup"><span data-stu-id="9462c-113">PARAMETERS</span></span>

### <span data-ttu-id="9462c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9462c-114">-DefaultProfile</span></span>
<span data-ttu-id="9462c-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9462c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9462c-116">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9462c-116">-ObjectId</span></span>
<span data-ttu-id="9462c-117">A ID de objeto da entidade de serviço para a qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="9462c-117">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9462c-118">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="9462c-118">-ServicePrincipalName</span></span>
<span data-ttu-id="9462c-119">O nome (SPN) da entidade de serviço para a qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="9462c-119">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9462c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9462c-120">CommonParameters</span></span>
<span data-ttu-id="9462c-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9462c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9462c-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9462c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9462c-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9462c-123">INPUTS</span></span>

### <span data-ttu-id="9462c-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9462c-124">None</span></span>
<span data-ttu-id="9462c-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9462c-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9462c-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9462c-126">OUTPUTS</span></span>

### <span data-ttu-id="9462c-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="9462c-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="9462c-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9462c-128">NOTES</span></span>

## <span data-ttu-id="9462c-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9462c-129">RELATED LINKS</span></span>

[<span data-ttu-id="9462c-130">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9462c-130">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="9462c-131">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9462c-131">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="9462c-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9462c-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

