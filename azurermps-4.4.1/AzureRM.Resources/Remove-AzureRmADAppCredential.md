---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: a5e99f045701a373e14990c25627696d40a04a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432560"
---
# <span data-ttu-id="93974-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="93974-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="93974-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93974-102">SYNOPSIS</span></span>
<span data-ttu-id="93974-103">Remove uma credencial de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93974-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93974-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93974-104">SYNTAX</span></span>

### <span data-ttu-id="93974-105">ApplicationObjectIdWithKeyIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="93974-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93974-106">ApplicationObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="93974-106">ApplicationObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93974-107">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93974-107">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93974-108">ApplicationIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="93974-108">ApplicationIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93974-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93974-109">DESCRIPTION</span></span>
<span data-ttu-id="93974-110">O cmdlet Remove-AzureRmADAppCredential pode ser usado para remover uma chave de credencial de um aplicativo no caso de um comprometimento ou como parte da expiração da sobreposição da chave da credencial.</span><span class="sxs-lookup"><span data-stu-id="93974-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="93974-111">O aplicativo é identificado fornecendo o ID do objeto ou AppId.</span><span class="sxs-lookup"><span data-stu-id="93974-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="93974-112">A credencial a ser removida é identificada pela ID da chave se uma credencial individual for removida ou com uma opção ' all' para excluir todas as credenciais associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93974-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the application.</span></span>

## <span data-ttu-id="93974-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93974-113">EXAMPLES</span></span>

### <span data-ttu-id="93974-114">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="93974-114">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="93974-115">Esse comando Remove uma chave de credencial de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93974-115">This command removes a credential key from an application.</span></span>
<span data-ttu-id="93974-116">Neste exemplo, a chave com ID "9044423a-60a3-45ac-9ab1-09534157ebb" será removida do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93974-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the application.</span></span>

### <span data-ttu-id="93974-117">--------------------------Exemplo 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="93974-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

<span data-ttu-id="93974-118">Esse comando Remove uma chave de credencial de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93974-118">This command removes a credential key from an application.</span></span>
<span data-ttu-id="93974-119">Neste exemplo, todas as credenciais serão removidas do aplicativo associado à applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="93974-119">In this example, all credentials will be removed from the application associated with the applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span></span>

## <span data-ttu-id="93974-120">OS</span><span class="sxs-lookup"><span data-stu-id="93974-120">PARAMETERS</span></span>

### <span data-ttu-id="93974-121">-Tudo</span><span class="sxs-lookup"><span data-stu-id="93974-121">-All</span></span>
<span data-ttu-id="93974-122">Alternar para remover todas as credenciais associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93974-122">Switch to remove all the credentials associated with the application.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93974-123">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="93974-123">-ApplicationId</span></span>
<span data-ttu-id="93974-124">A ID do aplicativo do qual as credenciais será removida.</span><span class="sxs-lookup"><span data-stu-id="93974-124">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93974-125">-Force</span><span class="sxs-lookup"><span data-stu-id="93974-125">-Force</span></span>
<span data-ttu-id="93974-126">Alternar para excluir credencial sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="93974-126">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93974-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="93974-127">-KeyId</span></span>
<span data-ttu-id="93974-128">Especifica a chave de credencial a ser removida.</span><span class="sxs-lookup"><span data-stu-id="93974-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="93974-129">As IDs de chave do aplicativo podem ser obtidas usando o cmdlet Get-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="93974-129">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93974-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="93974-130">-ObjectId</span></span>
<span data-ttu-id="93974-131">A ID de objeto do aplicativo do qual as credenciais será removida.</span><span class="sxs-lookup"><span data-stu-id="93974-131">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93974-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="93974-132">-Confirm</span></span>
<span data-ttu-id="93974-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93974-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93974-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93974-134">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93974-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93974-135">-DefaultProfile</span></span>
<span data-ttu-id="93974-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93974-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93974-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93974-137">CommonParameters</span></span>
<span data-ttu-id="93974-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93974-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93974-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93974-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93974-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93974-140">INPUTS</span></span>

## <span data-ttu-id="93974-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93974-141">OUTPUTS</span></span>

## <span data-ttu-id="93974-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93974-142">NOTES</span></span>

## <span data-ttu-id="93974-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93974-143">RELATED LINKS</span></span>

[<span data-ttu-id="93974-144">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="93974-144">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="93974-145">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="93974-145">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="93974-146">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="93974-146">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
