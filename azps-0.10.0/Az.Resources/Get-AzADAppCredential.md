---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: fc8e454328706243e701c0f4df61733562ab73ce
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776464"
---
# <span data-ttu-id="8a8c2-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8a8c2-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="8a8c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a8c2-102">SYNOPSIS</span></span>
<span data-ttu-id="8a8c2-103">Recupera uma lista de credenciais associadas a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8a8c2-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="8a8c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a8c2-104">SYNTAX</span></span>

### <span data-ttu-id="8a8c2-105">ApplicationObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8a8c2-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a8c2-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a8c2-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a8c2-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a8c2-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a8c2-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a8c2-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a8c2-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a8c2-109">DESCRIPTION</span></span>
<span data-ttu-id="8a8c2-110">O cmdlet Get-AzADAppCredential pode ser usado para recuperar uma lista de credenciais associadas a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8a8c2-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="8a8c2-111">Esse comando recuperará todas as propriedades de credenciais (mas não o valor da credencial) associado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8a8c2-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="8a8c2-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a8c2-112">EXAMPLES</span></span>

### <span data-ttu-id="8a8c2-113">Exemplo 1-obter credenciais do aplicativo por ID do objeto</span><span class="sxs-lookup"><span data-stu-id="8a8c2-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="8a8c2-114">Retorna uma lista de credenciais associadas ao aplicativo com a ID de objeto ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 '.</span><span class="sxs-lookup"><span data-stu-id="8a8c2-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="8a8c2-115">Exemplo 2-obter credenciais de aplicativo por tubulação</span><span class="sxs-lookup"><span data-stu-id="8a8c2-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="8a8c2-116">Obtém o aplicativo com a ID de objeto ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 ' e a canaliza para o cmdlet Get-AzADAppCredential para listar todas as credenciais desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8a8c2-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="8a8c2-117">OS</span><span class="sxs-lookup"><span data-stu-id="8a8c2-117">PARAMETERS</span></span>

### <span data-ttu-id="8a8c2-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8a8c2-118">-ApplicationId</span></span>
<span data-ttu-id="8a8c2-119">A ID do aplicativo do qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="8a8c2-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="8a8c2-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="8a8c2-120">-ApplicationObject</span></span>
<span data-ttu-id="8a8c2-121">O objeto de aplicativo do qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="8a8c2-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a8c2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a8c2-122">-DefaultProfile</span></span>
<span data-ttu-id="8a8c2-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8a8c2-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8c2-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8a8c2-124">-DisplayName</span></span>
<span data-ttu-id="8a8c2-125">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8a8c2-125">The display name of the application.</span></span>

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

### <span data-ttu-id="8a8c2-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8a8c2-126">-ObjectId</span></span>
<span data-ttu-id="8a8c2-127">A ID de objeto do aplicativo do qual as credenciais são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="8a8c2-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="8a8c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a8c2-128">CommonParameters</span></span>
<span data-ttu-id="8a8c2-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a8c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a8c2-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a8c2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a8c2-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a8c2-131">INPUTS</span></span>

### <span data-ttu-id="8a8c2-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8a8c2-132">System.Guid</span></span>

### <span data-ttu-id="8a8c2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8a8c2-133">System.String</span></span>

### <span data-ttu-id="8a8c2-134">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="8a8c2-134">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="8a8c2-135">Parâmetros: applicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8a8c2-135">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="8a8c2-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a8c2-136">OUTPUTS</span></span>

### <span data-ttu-id="8a8c2-137">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="8a8c2-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="8a8c2-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a8c2-138">NOTES</span></span>

## <span data-ttu-id="8a8c2-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a8c2-139">RELATED LINKS</span></span>

[<span data-ttu-id="8a8c2-140">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8a8c2-140">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="8a8c2-141">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8a8c2-141">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="8a8c2-142">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8a8c2-142">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
