---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: 7bfa908e83d7731ca2ed5613d82f42b19c392b2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112175"
---
# <span data-ttu-id="0ba37-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0ba37-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="0ba37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ba37-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba37-103">Recupera uma lista de credenciais associadas a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0ba37-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="0ba37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ba37-104">SYNTAX</span></span>

### <span data-ttu-id="0ba37-105">ApplicationObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0ba37-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ba37-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ba37-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ba37-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ba37-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ba37-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ba37-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ba37-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0ba37-109">DESCRIPTION</span></span>
<span data-ttu-id="0ba37-110">O cmdlet Get-AzADAppCredential pode ser usado para recuperar uma lista de credenciais associadas a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0ba37-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="0ba37-111">Esse comando recuperará todas as propriedades de credenciais (mas não o valor da credencial) associado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0ba37-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="0ba37-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ba37-112">EXAMPLES</span></span>

### <span data-ttu-id="0ba37-113">Exemplo 1: obter credenciais do aplicativo por ID do objeto</span><span class="sxs-lookup"><span data-stu-id="0ba37-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="0ba37-114">Retorna uma lista de credenciais associadas ao aplicativo com a ID de objeto ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 '.</span><span class="sxs-lookup"><span data-stu-id="0ba37-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="0ba37-115">Exemplo 2: obter credenciais de aplicativo por tubulação</span><span class="sxs-lookup"><span data-stu-id="0ba37-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="0ba37-116">Obtém o aplicativo com a ID de objeto ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 ' e a canaliza para o cmdlet Get-AzADAppCredential para listar todas as credenciais desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0ba37-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="0ba37-117">OS</span><span class="sxs-lookup"><span data-stu-id="0ba37-117">PARAMETERS</span></span>

### <span data-ttu-id="0ba37-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0ba37-118">-ApplicationId</span></span>
<span data-ttu-id="0ba37-119">A ID do aplicativo do qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="0ba37-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="0ba37-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="0ba37-120">-ApplicationObject</span></span>
<span data-ttu-id="0ba37-121">O objeto de aplicativo do qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="0ba37-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="0ba37-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba37-122">-DefaultProfile</span></span>
<span data-ttu-id="0ba37-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0ba37-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ba37-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0ba37-124">-DisplayName</span></span>
<span data-ttu-id="0ba37-125">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0ba37-125">The display name of the application.</span></span>

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

### <span data-ttu-id="0ba37-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0ba37-126">-ObjectId</span></span>
<span data-ttu-id="0ba37-127">A ID de objeto do aplicativo do qual as credenciais são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="0ba37-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="0ba37-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba37-128">CommonParameters</span></span>
<span data-ttu-id="0ba37-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ba37-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba37-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ba37-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba37-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0ba37-131">INPUTS</span></span>

### <span data-ttu-id="0ba37-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0ba37-132">System.String</span></span>

### <span data-ttu-id="0ba37-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0ba37-133">System.Guid</span></span>

### <span data-ttu-id="0ba37-134">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="0ba37-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="0ba37-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0ba37-135">OUTPUTS</span></span>

### <span data-ttu-id="0ba37-136">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="0ba37-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="0ba37-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0ba37-137">NOTES</span></span>

## <span data-ttu-id="0ba37-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ba37-138">RELATED LINKS</span></span>

[<span data-ttu-id="0ba37-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0ba37-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="0ba37-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0ba37-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="0ba37-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="0ba37-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

