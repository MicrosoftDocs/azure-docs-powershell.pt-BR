---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: fdef07255316b1d7529202c36b844e8732c76390
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772612"
---
# <span data-ttu-id="e4b21-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e4b21-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="e4b21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4b21-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b21-103">Recupera uma lista de credenciais associadas a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e4b21-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="e4b21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4b21-104">SYNTAX</span></span>

### <span data-ttu-id="e4b21-105">ApplicationObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e4b21-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4b21-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4b21-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4b21-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4b21-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4b21-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4b21-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4b21-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4b21-109">DESCRIPTION</span></span>
<span data-ttu-id="e4b21-110">O cmdlet Get-AzADAppCredential pode ser usado para recuperar uma lista de credenciais associadas a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e4b21-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="e4b21-111">Esse comando recuperará todas as propriedades de credenciais (mas não o valor da credencial) associado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e4b21-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="e4b21-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4b21-112">EXAMPLES</span></span>

### <span data-ttu-id="e4b21-113">Exemplo 1-obter credenciais do aplicativo por ID do objeto</span><span class="sxs-lookup"><span data-stu-id="e4b21-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="e4b21-114">Retorna uma lista de credenciais associadas ao aplicativo com a ID de objeto ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 '.</span><span class="sxs-lookup"><span data-stu-id="e4b21-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="e4b21-115">Exemplo 2-obter credenciais de aplicativo por tubulação</span><span class="sxs-lookup"><span data-stu-id="e4b21-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="e4b21-116">Obtém o aplicativo com a ID de objeto ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 ' e a canaliza para o cmdlet Get-AzADAppCredential para listar todas as credenciais desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e4b21-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="e4b21-117">OS</span><span class="sxs-lookup"><span data-stu-id="e4b21-117">PARAMETERS</span></span>

### <span data-ttu-id="e4b21-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e4b21-118">-ApplicationId</span></span>
<span data-ttu-id="e4b21-119">A ID do aplicativo do qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="e4b21-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="e4b21-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="e4b21-120">-ApplicationObject</span></span>
<span data-ttu-id="e4b21-121">O objeto de aplicativo do qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="e4b21-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="e4b21-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b21-122">-DefaultProfile</span></span>
<span data-ttu-id="e4b21-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e4b21-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4b21-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e4b21-124">-DisplayName</span></span>
<span data-ttu-id="e4b21-125">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e4b21-125">The display name of the application.</span></span>

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

### <span data-ttu-id="e4b21-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e4b21-126">-ObjectId</span></span>
<span data-ttu-id="e4b21-127">A ID de objeto do aplicativo do qual as credenciais são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="e4b21-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="e4b21-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b21-128">CommonParameters</span></span>
<span data-ttu-id="e4b21-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4b21-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b21-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4b21-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b21-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4b21-131">INPUTS</span></span>

### <span data-ttu-id="e4b21-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e4b21-132">System.String</span></span>

### <span data-ttu-id="e4b21-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e4b21-133">System.Guid</span></span>

### <span data-ttu-id="e4b21-134">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e4b21-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e4b21-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4b21-135">OUTPUTS</span></span>

### <span data-ttu-id="e4b21-136">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="e4b21-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="e4b21-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4b21-137">NOTES</span></span>

## <span data-ttu-id="e4b21-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4b21-138">RELATED LINKS</span></span>

[<span data-ttu-id="e4b21-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e4b21-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="e4b21-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e4b21-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="e4b21-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e4b21-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
