---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: b1f4b8d53a1031cef76d51a87bbf9afa5b75758f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610189"
---
# <span data-ttu-id="1a84b-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1a84b-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="1a84b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a84b-102">SYNOPSIS</span></span>
<span data-ttu-id="1a84b-103">Remove uma credencial de uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="1a84b-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a84b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a84b-104">SYNTAX</span></span>

### <span data-ttu-id="1a84b-105">ObjectIdWithKeyIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1a84b-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a84b-106">ObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a84b-106">ObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a84b-107">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a84b-107">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a84b-108">SPNWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a84b-108">SPNWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a84b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a84b-109">DESCRIPTION</span></span>
<span data-ttu-id="1a84b-110">O cmdlet Remove-AzureRmADSpCredential pode ser usado para remover uma chave de credencial de uma entidade de serviço no caso de um comprometimento ou como parte da expiração da sobreposição da chave da credencial.</span><span class="sxs-lookup"><span data-stu-id="1a84b-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="1a84b-111">A entidade de serviço é identificada fornecendo a identificação do objeto ou o SPN (nome da entidade de serviço).</span><span class="sxs-lookup"><span data-stu-id="1a84b-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>

<span data-ttu-id="1a84b-112">A credencial a ser removida é identificada pela ID da chave se uma credencial individual for removida ou com uma opção ' all' para excluir todas as credenciais associadas à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="1a84b-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="1a84b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a84b-113">EXAMPLES</span></span>

### <span data-ttu-id="1a84b-114">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1a84b-114">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="1a84b-115">Esse comando Remove uma chave de credencial de uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="1a84b-115">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="1a84b-116">Neste exemplo, a chave com ID "9044423a-60a3-45ac-9ab1-09534157ebb" será removida da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="1a84b-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the service principal.</span></span>

### <span data-ttu-id="1a84b-117">--------------------------Exemplo 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1a84b-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

<span data-ttu-id="1a84b-118">Esse comando Remove uma chave de credencial de uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="1a84b-118">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="1a84b-119">Neste exemplo, todas as credenciais serão removidas da entidade de serviço associada ao nome principal do serviço " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="1a84b-119">In this example, all credentials will be removed from the service principal associated with the service principal name "http://test123".</span></span>

## <span data-ttu-id="1a84b-120">OS</span><span class="sxs-lookup"><span data-stu-id="1a84b-120">PARAMETERS</span></span>

### <span data-ttu-id="1a84b-121">-Tudo</span><span class="sxs-lookup"><span data-stu-id="1a84b-121">-All</span></span>
<span data-ttu-id="1a84b-122">Alterne para remover todas as credenciais associadas à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="1a84b-122">Switch to remove all the credentials associated with the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a84b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1a84b-123">-Force</span></span>
<span data-ttu-id="1a84b-124">Alternar para excluir credencial sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="1a84b-124">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="1a84b-125">-KeyId</span><span class="sxs-lookup"><span data-stu-id="1a84b-125">-KeyId</span></span>
<span data-ttu-id="1a84b-126">Especifica a chave de credencial a ser removida.</span><span class="sxs-lookup"><span data-stu-id="1a84b-126">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="1a84b-127">As IDs de chave para uma entidade de serviço podem ser obtidas usando o cmdlet Get-AzureRmADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="1a84b-127">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a84b-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1a84b-128">-ObjectId</span></span>
<span data-ttu-id="1a84b-129">A ID de objeto da entidade de serviço para a qual as credenciais são removidas.</span><span class="sxs-lookup"><span data-stu-id="1a84b-129">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a84b-130">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="1a84b-130">-ServicePrincipalName</span></span>
<span data-ttu-id="1a84b-131">O nome (SPN) da entidade de serviço para a qual remover as credenciais.</span><span class="sxs-lookup"><span data-stu-id="1a84b-131">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a84b-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a84b-132">-Confirm</span></span>
<span data-ttu-id="1a84b-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a84b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a84b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a84b-134">-WhatIf</span></span>
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

### <span data-ttu-id="1a84b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a84b-135">-DefaultProfile</span></span>
<span data-ttu-id="1a84b-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a84b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a84b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a84b-137">CommonParameters</span></span>
<span data-ttu-id="1a84b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a84b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a84b-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a84b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a84b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a84b-140">INPUTS</span></span>

## <span data-ttu-id="1a84b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a84b-141">OUTPUTS</span></span>

## <span data-ttu-id="1a84b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a84b-142">NOTES</span></span>

## <span data-ttu-id="1a84b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a84b-143">RELATED LINKS</span></span>

[<span data-ttu-id="1a84b-144">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1a84b-144">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="1a84b-145">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1a84b-145">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="1a84b-146">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1a84b-146">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

