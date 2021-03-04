---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: c96fceb331a2b33528b47506e928ea78cfc793d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888195"
---
# <span data-ttu-id="84e0b-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="84e0b-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="84e0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="84e0b-103">Recupera uma lista de credenciais associadas a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="84e0b-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="84e0b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="84e0b-104">SYNTAX</span></span>

### <span data-ttu-id="84e0b-105">ApplicationObjectIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="84e0b-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84e0b-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84e0b-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84e0b-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="84e0b-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84e0b-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84e0b-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84e0b-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="84e0b-109">DESCRIPTION</span></span>
<span data-ttu-id="84e0b-110">O Get-AzADAppCredential cmdlet pode ser usado para recuperar uma lista de credenciais associadas a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="84e0b-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="84e0b-111">Esse comando recuperará todas as propriedades de credencial (mas não o valor de credencial) associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="84e0b-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="84e0b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84e0b-112">EXAMPLES</span></span>

### <span data-ttu-id="84e0b-113">Exemplo 1: Obter credenciais de aplicativo por id de objeto</span><span class="sxs-lookup"><span data-stu-id="84e0b-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="84e0b-114">Retorna uma lista de credenciais associadas ao aplicativo com a id do objeto '1f99cf81-0146-4f4e-beae-2007d0668476'.</span><span class="sxs-lookup"><span data-stu-id="84e0b-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="84e0b-115">Exemplo 2: Obter credenciais de aplicativo por canalização</span><span class="sxs-lookup"><span data-stu-id="84e0b-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="84e0b-116">Obtém o aplicativo com a id do objeto '1f99cf81-0146-4f4e-beae-2007d0668476' e canalizará-o para o cmdlet Get-AzADAppCredential para listar todas as credenciais desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="84e0b-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="84e0b-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="84e0b-117">PARAMETERS</span></span>

### <span data-ttu-id="84e0b-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="84e0b-118">-ApplicationId</span></span>
<span data-ttu-id="84e0b-119">A id do aplicativo para recuperar credenciais.</span><span class="sxs-lookup"><span data-stu-id="84e0b-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="84e0b-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="84e0b-120">-ApplicationObject</span></span>
<span data-ttu-id="84e0b-121">O objeto application para recuperar credenciais.</span><span class="sxs-lookup"><span data-stu-id="84e0b-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84e0b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e0b-122">-DefaultProfile</span></span>
<span data-ttu-id="84e0b-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="84e0b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84e0b-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="84e0b-124">-DisplayName</span></span>
<span data-ttu-id="84e0b-125">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="84e0b-125">The display name of the application.</span></span>

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

### <span data-ttu-id="84e0b-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="84e0b-126">-ObjectId</span></span>
<span data-ttu-id="84e0b-127">A ID do objeto do aplicativo para recuperar credenciais.</span><span class="sxs-lookup"><span data-stu-id="84e0b-127">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84e0b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e0b-128">CommonParameters</span></span>
<span data-ttu-id="84e0b-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84e0b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e0b-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84e0b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e0b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84e0b-131">INPUTS</span></span>

### <span data-ttu-id="84e0b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="84e0b-132">System.String</span></span>

### <span data-ttu-id="84e0b-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="84e0b-133">System.Guid</span></span>

### <span data-ttu-id="84e0b-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="84e0b-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="84e0b-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="84e0b-135">OUTPUTS</span></span>

### <span data-ttu-id="84e0b-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="84e0b-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="84e0b-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="84e0b-137">NOTES</span></span>

## <span data-ttu-id="84e0b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84e0b-138">RELATED LINKS</span></span>

[<span data-ttu-id="84e0b-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="84e0b-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="84e0b-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="84e0b-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="84e0b-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="84e0b-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

