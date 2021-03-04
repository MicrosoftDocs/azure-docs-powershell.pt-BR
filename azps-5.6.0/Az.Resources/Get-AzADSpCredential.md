---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 83212224ba14e0a079db936d058522d4759430fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886598"
---
# <span data-ttu-id="68579-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="68579-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="68579-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68579-102">SYNOPSIS</span></span>
<span data-ttu-id="68579-103">Recupera uma lista de credenciais associadas a uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="68579-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="68579-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="68579-104">SYNTAX</span></span>

### <span data-ttu-id="68579-105">ObjectIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="68579-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68579-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="68579-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68579-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="68579-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68579-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68579-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68579-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="68579-109">DESCRIPTION</span></span>
<span data-ttu-id="68579-110">O Get-AzADSpCredential cmdlet pode ser usado para recuperar uma lista de credenciais associadas a uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="68579-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="68579-111">Este comando recuperará todas as propriedades de credencial (mas não o valor de credencial) associadas à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="68579-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="68579-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68579-112">EXAMPLES</span></span>

### <span data-ttu-id="68579-113">Exemplo 1 - Listar credenciais pelo SPN</span><span class="sxs-lookup"><span data-stu-id="68579-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="68579-114">Retorna uma lista de credenciais associadas à entidade de serviço com o SPN http://test12345 ' '.</span><span class="sxs-lookup"><span data-stu-id="68579-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="68579-115">Exemplo 2 - Listar credenciais por id de objeto</span><span class="sxs-lookup"><span data-stu-id="68579-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="68579-116">Retorna uma lista de credenciais associadas à entidade de serviço com a id do objeto "58e28616-99cc-4da4-b705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="68579-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="68579-117">Exemplo 3 - Listar credenciais por canalização</span><span class="sxs-lookup"><span data-stu-id="68579-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="68579-118">Obtém a entidade de serviço com a id do objeto "58e28616-99cc-4da4-b705-7672130e1047" e canalizará-a para o cmdlet Get-AzADSpCredential para listar todas as credenciais dessa entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="68579-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="68579-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="68579-119">PARAMETERS</span></span>

### <span data-ttu-id="68579-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68579-120">-DefaultProfile</span></span>
<span data-ttu-id="68579-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="68579-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68579-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="68579-122">-DisplayName</span></span>
<span data-ttu-id="68579-123">O nome de exibição da entidade de serviço</span><span class="sxs-lookup"><span data-stu-id="68579-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="68579-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="68579-124">-ObjectId</span></span>
<span data-ttu-id="68579-125">A ID do objeto da entidade de serviço a ser recuperada de credenciais.</span><span class="sxs-lookup"><span data-stu-id="68579-125">The object id of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="68579-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="68579-126">-ServicePrincipalName</span></span>
<span data-ttu-id="68579-127">O nome (SPN) da entidade de serviço a ser recuperada de credenciais.</span><span class="sxs-lookup"><span data-stu-id="68579-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="68579-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="68579-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="68579-129">O objeto principal do serviço para recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="68579-129">The service principal object to retrieve the credentials from.</span></span>

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

### <span data-ttu-id="68579-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68579-130">CommonParameters</span></span>
<span data-ttu-id="68579-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68579-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68579-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68579-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68579-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68579-133">INPUTS</span></span>

### <span data-ttu-id="68579-134">System.String</span><span class="sxs-lookup"><span data-stu-id="68579-134">System.String</span></span>

### <span data-ttu-id="68579-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="68579-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="68579-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="68579-136">OUTPUTS</span></span>

### <span data-ttu-id="68579-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="68579-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="68579-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="68579-138">NOTES</span></span>

## <span data-ttu-id="68579-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68579-139">RELATED LINKS</span></span>

[<span data-ttu-id="68579-140">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="68579-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="68579-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="68579-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="68579-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="68579-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

