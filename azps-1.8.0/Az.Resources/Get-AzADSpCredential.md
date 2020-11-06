---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 5307e070f8c568473e1ce35f1183517cd3def05c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599449"
---
# <span data-ttu-id="ea1a4-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ea1a4-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="ea1a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea1a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ea1a4-103">Recupera uma lista de credenciais associadas a uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ea1a4-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="ea1a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea1a4-104">SYNTAX</span></span>

### <span data-ttu-id="ea1a4-105">ObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ea1a4-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea1a4-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1a4-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea1a4-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1a4-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea1a4-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1a4-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea1a4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea1a4-109">DESCRIPTION</span></span>
<span data-ttu-id="ea1a4-110">O cmdlet Get-AzADSpCredential pode ser usado para recuperar uma lista de credenciais associadas a uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ea1a4-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="ea1a4-111">Esse comando recuperará todas as propriedades de credenciais (mas não o valor da credencial) associados à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ea1a4-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="ea1a4-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea1a4-112">EXAMPLES</span></span>

### <span data-ttu-id="ea1a4-113">Exemplo 1-listar credenciais por SPN</span><span class="sxs-lookup"><span data-stu-id="ea1a4-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="ea1a4-114">Retorna uma lista de credenciais associadas à entidade de serviço com SPN ' http://test12345 '.</span><span class="sxs-lookup"><span data-stu-id="ea1a4-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="ea1a4-115">Exemplo 2-listar credenciais por ID do objeto</span><span class="sxs-lookup"><span data-stu-id="ea1a4-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="ea1a4-116">Retorna uma lista de credenciais associadas à entidade de serviço com a ID de objeto "58e28616-99cc-4DA4-b705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="ea1a4-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="ea1a4-117">Exemplo de 3-listar credenciais por tubulação</span><span class="sxs-lookup"><span data-stu-id="ea1a4-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="ea1a4-118">Obtém a entidade de serviço com a ID de objeto "58e28616-99cc-4DA4-b705-7672130e1047" e a canaliza para o cmdlet Get-AzADSpCredential para listar todas as credenciais para essa entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="ea1a4-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="ea1a4-119">OS</span><span class="sxs-lookup"><span data-stu-id="ea1a4-119">PARAMETERS</span></span>

### <span data-ttu-id="ea1a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea1a4-120">-DefaultProfile</span></span>
<span data-ttu-id="ea1a4-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ea1a4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a4-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ea1a4-122">-DisplayName</span></span>
<span data-ttu-id="ea1a4-123">O nome de exibição da entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="ea1a4-123">The display name of the service principal</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a4-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ea1a4-124">-ObjectId</span></span>
<span data-ttu-id="ea1a4-125">A ID de objeto da entidade de serviço para a qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="ea1a4-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a4-126">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="ea1a4-126">-ServicePrincipalName</span></span>
<span data-ttu-id="ea1a4-127">O nome (SPN) da entidade de serviço para a qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="ea1a4-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a4-128">-Serviceprincipalnameobject</span><span class="sxs-lookup"><span data-stu-id="ea1a4-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="ea1a4-129">O objeto de entidade de serviço para o qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="ea1a4-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea1a4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea1a4-130">CommonParameters</span></span>
<span data-ttu-id="ea1a4-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea1a4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea1a4-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea1a4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea1a4-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea1a4-133">INPUTS</span></span>

### <span data-ttu-id="ea1a4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ea1a4-134">System.String</span></span>

### <span data-ttu-id="ea1a4-135">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ea1a4-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="ea1a4-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea1a4-136">OUTPUTS</span></span>

### <span data-ttu-id="ea1a4-137">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="ea1a4-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="ea1a4-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea1a4-138">NOTES</span></span>

## <span data-ttu-id="ea1a4-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea1a4-139">RELATED LINKS</span></span>

[<span data-ttu-id="ea1a4-140">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ea1a4-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="ea1a4-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ea1a4-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="ea1a4-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ea1a4-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

