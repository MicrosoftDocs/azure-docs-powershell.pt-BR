---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: a8c1aa2d0f22a9c6dc6260384e51140cb930106a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433434"
---
# <span data-ttu-id="4bd03-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4bd03-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="4bd03-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4bd03-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd03-103">Atualiza um aplicativo existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4bd03-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bd03-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4bd03-104">SYNTAX</span></span>

### <span data-ttu-id="4bd03-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bd03-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bd03-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bd03-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bd03-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4bd03-107">DESCRIPTION</span></span>
<span data-ttu-id="4bd03-108">Atualiza um aplicativo existente do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4bd03-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="4bd03-109">Para atualizar as credenciais associadas a esse aplicativo, use o cmdlet New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="4bd03-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="4bd03-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4bd03-110">EXAMPLES</span></span>

### <span data-ttu-id="4bd03-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4bd03-111">Example 1</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="4bd03-112">Atualiza as propriedades de um aplicativo existente do Azure Active Directory com objectId "fb7b3405-ca44-4B5B-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="4bd03-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="4bd03-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4bd03-113">Example 2</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="4bd03-114">Atualiza o nome de exibição de um aplicativo do Azure Active Directory existente com objectId "fb7b3405-ca44-4B5B-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="4bd03-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="4bd03-115">OS</span><span class="sxs-lookup"><span data-stu-id="4bd03-115">PARAMETERS</span></span>

### <span data-ttu-id="4bd03-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4bd03-116">-ApplicationId</span></span>
<span data-ttu-id="4bd03-117">A ID do aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="4bd03-117">The id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd03-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="4bd03-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="4bd03-119">O valor que especifica se o aplicativo é atualizado para ser um único locatário ou um multi-locatário.</span><span class="sxs-lookup"><span data-stu-id="4bd03-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd03-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd03-120">-DefaultProfile</span></span>
<span data-ttu-id="4bd03-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4bd03-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd03-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4bd03-122">-DisplayName</span></span>
<span data-ttu-id="4bd03-123">Novo nome para exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4bd03-123">New Display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd03-124">-Página inicial</span><span class="sxs-lookup"><span data-stu-id="4bd03-124">-HomePage</span></span>
<span data-ttu-id="4bd03-125">Nova URL da página inicial do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4bd03-125">New URL of the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd03-126">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="4bd03-126">-IdentifierUris</span></span>
<span data-ttu-id="4bd03-127">Novos URIs que identificam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4bd03-127">New URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd03-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4bd03-128">-ObjectId</span></span>
<span data-ttu-id="4bd03-129">A ID de objeto do aplicativo a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="4bd03-129">The object id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd03-130">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="4bd03-130">-ReplyUrls</span></span>
<span data-ttu-id="4bd03-131">Novas URLs de resposta para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4bd03-131">New reply urls for the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd03-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4bd03-132">-Confirm</span></span>
<span data-ttu-id="4bd03-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bd03-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd03-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bd03-134">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd03-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd03-135">CommonParameters</span></span>
<span data-ttu-id="4bd03-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd03-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd03-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd03-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd03-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4bd03-138">INPUTS</span></span>

### <span data-ttu-id="4bd03-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4bd03-139">None</span></span>
<span data-ttu-id="4bd03-140">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4bd03-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4bd03-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4bd03-141">OUTPUTS</span></span>

### <span data-ttu-id="4bd03-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="4bd03-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="4bd03-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4bd03-143">NOTES</span></span>

## <span data-ttu-id="4bd03-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4bd03-144">RELATED LINKS</span></span>

[<span data-ttu-id="4bd03-145">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4bd03-145">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="4bd03-146">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4bd03-146">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="4bd03-147">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4bd03-147">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="4bd03-148">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4bd03-148">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="4bd03-149">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4bd03-149">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="4bd03-150">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4bd03-150">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

