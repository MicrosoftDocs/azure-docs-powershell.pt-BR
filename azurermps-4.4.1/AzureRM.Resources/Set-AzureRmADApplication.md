---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: 6fbbed83f9565a81b305df5cf8b66fd8210c6aec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610721"
---
# <span data-ttu-id="67b21-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="67b21-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="67b21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67b21-102">SYNOPSIS</span></span>
<span data-ttu-id="67b21-103">Atualiza um aplicativo existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="67b21-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67b21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67b21-104">SYNTAX</span></span>

### <span data-ttu-id="67b21-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b21-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67b21-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b21-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67b21-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67b21-107">DESCRIPTION</span></span>
<span data-ttu-id="67b21-108">Atualiza um aplicativo existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="67b21-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="67b21-109">Para atualizar as credenciais associadas a esse aplicativo, use o cmdlet New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="67b21-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="67b21-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67b21-110">EXAMPLES</span></span>

### <span data-ttu-id="67b21-111">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="67b21-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="67b21-112">Atualiza as propriedades de um aplicativo existente do Azure Active Directory com objectId "fb7b3405-ca44-4B5B-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="67b21-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="67b21-113">--------------------------Exemplo 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="67b21-113">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="67b21-114">Atualiza o nome de exibição de um aplicativo do Azure Active Directory existente com objectId "fb7b3405-ca44-4B5B-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="67b21-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="67b21-115">OS</span><span class="sxs-lookup"><span data-stu-id="67b21-115">PARAMETERS</span></span>

### <span data-ttu-id="67b21-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="67b21-116">-ApplicationId</span></span>
<span data-ttu-id="67b21-117">A ID do aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="67b21-117">The id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b21-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="67b21-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="67b21-119">O valor que especifica se o aplicativo é atualizado para ser um único locatário ou um multi-locatário.</span><span class="sxs-lookup"><span data-stu-id="67b21-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b21-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="67b21-120">-DisplayName</span></span>
<span data-ttu-id="67b21-121">Novo nome para exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67b21-121">New Display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b21-122">-Página inicial</span><span class="sxs-lookup"><span data-stu-id="67b21-122">-HomePage</span></span>
<span data-ttu-id="67b21-123">Nova URL da página inicial do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67b21-123">New URL of the application homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b21-124">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="67b21-124">-IdentifierUris</span></span>
<span data-ttu-id="67b21-125">Novos URIs que identificam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67b21-125">New URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b21-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="67b21-126">-ObjectId</span></span>
<span data-ttu-id="67b21-127">A ID de objeto do aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="67b21-127">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b21-128">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="67b21-128">-ReplyUrls</span></span>
<span data-ttu-id="67b21-129">Novas URLs de resposta para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67b21-129">New reply urls for the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b21-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="67b21-130">-Confirm</span></span>
<span data-ttu-id="67b21-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67b21-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67b21-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67b21-132">-WhatIf</span></span>
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

### <span data-ttu-id="67b21-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b21-133">-DefaultProfile</span></span>
<span data-ttu-id="67b21-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67b21-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67b21-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b21-135">CommonParameters</span></span>
<span data-ttu-id="67b21-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67b21-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b21-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67b21-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b21-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67b21-138">INPUTS</span></span>

## <span data-ttu-id="67b21-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67b21-139">OUTPUTS</span></span>

### <span data-ttu-id="67b21-140">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="67b21-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="67b21-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67b21-141">NOTES</span></span>

## <span data-ttu-id="67b21-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67b21-142">RELATED LINKS</span></span>

[<span data-ttu-id="67b21-143">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="67b21-143">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="67b21-144">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="67b21-144">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="67b21-145">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="67b21-145">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="67b21-146">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="67b21-146">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="67b21-147">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="67b21-147">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="67b21-148">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="67b21-148">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

