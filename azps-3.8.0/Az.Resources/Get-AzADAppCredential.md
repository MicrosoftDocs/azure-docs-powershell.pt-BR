---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: ef03850e2a8c0981ad4a1b642df51c1fec462513
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942029"
---
# <span data-ttu-id="59b60-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="59b60-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="59b60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59b60-102">SYNOPSIS</span></span>
<span data-ttu-id="59b60-103">Recupera uma lista de credenciais associadas a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="59b60-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="59b60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59b60-104">SYNTAX</span></span>

### <span data-ttu-id="59b60-105">ApplicationObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="59b60-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59b60-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59b60-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59b60-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="59b60-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59b60-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59b60-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59b60-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59b60-109">DESCRIPTION</span></span>
<span data-ttu-id="59b60-110">O cmdlet Get-AzADAppCredential pode ser usado para recuperar uma lista de credenciais associadas a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="59b60-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="59b60-111">Esse comando recuperará todas as propriedades de credenciais (mas não o valor da credencial) associado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="59b60-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="59b60-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59b60-112">EXAMPLES</span></span>

### <span data-ttu-id="59b60-113">Exemplo 1-obter credenciais do aplicativo por ID do objeto</span><span class="sxs-lookup"><span data-stu-id="59b60-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="59b60-114">Retorna uma lista de credenciais associadas ao aplicativo com a ID de objeto ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 '.</span><span class="sxs-lookup"><span data-stu-id="59b60-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="59b60-115">Exemplo 2-obter credenciais de aplicativo por tubulação</span><span class="sxs-lookup"><span data-stu-id="59b60-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="59b60-116">Obtém o aplicativo com a ID de objeto ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 ' e a canaliza para o cmdlet Get-AzADAppCredential para listar todas as credenciais desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="59b60-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="59b60-117">OS</span><span class="sxs-lookup"><span data-stu-id="59b60-117">PARAMETERS</span></span>

### <span data-ttu-id="59b60-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="59b60-118">-ApplicationId</span></span>
<span data-ttu-id="59b60-119">A ID do aplicativo do qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="59b60-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="59b60-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="59b60-120">-ApplicationObject</span></span>
<span data-ttu-id="59b60-121">O objeto de aplicativo do qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="59b60-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="59b60-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b60-122">-DefaultProfile</span></span>
<span data-ttu-id="59b60-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="59b60-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59b60-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="59b60-124">-DisplayName</span></span>
<span data-ttu-id="59b60-125">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="59b60-125">The display name of the application.</span></span>

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

### <span data-ttu-id="59b60-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="59b60-126">-ObjectId</span></span>
<span data-ttu-id="59b60-127">A ID de objeto do aplicativo do qual as credenciais são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="59b60-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="59b60-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b60-128">CommonParameters</span></span>
<span data-ttu-id="59b60-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59b60-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b60-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59b60-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b60-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59b60-131">INPUTS</span></span>

### <span data-ttu-id="59b60-132">System. String</span><span class="sxs-lookup"><span data-stu-id="59b60-132">System.String</span></span>

### <span data-ttu-id="59b60-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="59b60-133">System.Guid</span></span>

### <span data-ttu-id="59b60-134">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="59b60-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="59b60-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59b60-135">OUTPUTS</span></span>

### <span data-ttu-id="59b60-136">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="59b60-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="59b60-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59b60-137">NOTES</span></span>

## <span data-ttu-id="59b60-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59b60-138">RELATED LINKS</span></span>

[<span data-ttu-id="59b60-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="59b60-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="59b60-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="59b60-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="59b60-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="59b60-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

