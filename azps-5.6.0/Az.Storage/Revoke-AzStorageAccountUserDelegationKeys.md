---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: 102f1ebc6152bb521bd1f9c7214a6c48ee61a274
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901555"
---
# <span data-ttu-id="573b8-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="573b8-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="573b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="573b8-102">SYNOPSIS</span></span>
<span data-ttu-id="573b8-103">Revogar todas as chaves de Delegação de Usuário de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="573b8-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="573b8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="573b8-104">SYNTAX</span></span>

### <span data-ttu-id="573b8-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="573b8-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="573b8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="573b8-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="573b8-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="573b8-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="573b8-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="573b8-108">DESCRIPTION</span></span>
<span data-ttu-id="573b8-109">O cmdlet **Revoke-AzStorageAccountUserDelegationKeys** revoga todas as chaves de Delegação de Usuário de uma conta de Armazenamento, portanto, todo o token SAS de identidade da conta de armazenamento também será revogado.</span><span class="sxs-lookup"><span data-stu-id="573b8-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="573b8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="573b8-110">EXAMPLES</span></span>

### <span data-ttu-id="573b8-111">Exemplo 1: Revogar todas as chaves de Delegação de Usuário de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="573b8-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="573b8-112">Este exemplo revoga todas as chaves de Delegação de Usuário de uma conta de Armazenamento, portanto, todos os tokens SAS de identidade gerados das chaves de Delegação de Usuário também serão revogados.</span><span class="sxs-lookup"><span data-stu-id="573b8-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="573b8-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="573b8-113">PARAMETERS</span></span>

### <span data-ttu-id="573b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="573b8-114">-DefaultProfile</span></span>
<span data-ttu-id="573b8-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="573b8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="573b8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="573b8-116">-InputObject</span></span>
<span data-ttu-id="573b8-117">Um objeto de conta de armazenamento, retornado por Get_AzStorageAccount, New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="573b8-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="573b8-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="573b8-118">-PassThru</span></span>
<span data-ttu-id="573b8-119">Normalmente, esse cmdlet retorna nenhuma saída após a conclusão bem-sucedida, este parâmetro força o cmdlet a retornar um valor ($true) na conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="573b8-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="573b8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="573b8-120">-ResourceGroupName</span></span>
<span data-ttu-id="573b8-121">O nome do grupo de recursos que contém o recurso de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="573b8-121">The resource group name containing the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573b8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="573b8-122">-ResourceId</span></span>
<span data-ttu-id="573b8-123">ID do Recurso de Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="573b8-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases: StorageAccountResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="573b8-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="573b8-124">-StorageAccountName</span></span>
<span data-ttu-id="573b8-125">O nome do recurso de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="573b8-125">The name of the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573b8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="573b8-126">-Confirm</span></span>
<span data-ttu-id="573b8-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="573b8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="573b8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="573b8-128">-WhatIf</span></span>
<span data-ttu-id="573b8-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="573b8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="573b8-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="573b8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="573b8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="573b8-131">CommonParameters</span></span>
<span data-ttu-id="573b8-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="573b8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="573b8-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="573b8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="573b8-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="573b8-134">INPUTS</span></span>

### <span data-ttu-id="573b8-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="573b8-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="573b8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="573b8-136">System.String</span></span>

## <span data-ttu-id="573b8-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="573b8-137">OUTPUTS</span></span>

### <span data-ttu-id="573b8-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="573b8-138">System.Boolean</span></span>

## <span data-ttu-id="573b8-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="573b8-139">NOTES</span></span>

## <span data-ttu-id="573b8-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="573b8-140">RELATED LINKS</span></span>
