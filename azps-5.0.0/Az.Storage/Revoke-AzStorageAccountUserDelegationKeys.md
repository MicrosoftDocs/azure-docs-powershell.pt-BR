---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115788"
---
# <span data-ttu-id="05af2-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="05af2-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="05af2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05af2-102">SYNOPSIS</span></span>
<span data-ttu-id="05af2-103">Revogar todas as chaves de delegação de usuário de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="05af2-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="05af2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05af2-104">SYNTAX</span></span>

### <span data-ttu-id="05af2-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="05af2-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05af2-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="05af2-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05af2-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="05af2-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05af2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05af2-108">DESCRIPTION</span></span>
<span data-ttu-id="05af2-109">O cmdlet **REVOKE-AzStorageAccountUserDelegationKeys** revoga todas as chaves de delegação de usuário de uma conta de armazenamento, para que todo o token SAS da identidade da conta de armazenamento também seja revogado.</span><span class="sxs-lookup"><span data-stu-id="05af2-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="05af2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05af2-110">EXAMPLES</span></span>

### <span data-ttu-id="05af2-111">Exemplo 1: revogar todas as chaves de delegação de usuário de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="05af2-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="05af2-112">Este exemplo revoga todas as chaves de delegação de usuário de uma conta de armazenamento, portanto, todo o token SAS de identidade gerado das chaves de delegação do usuário também será revogado.</span><span class="sxs-lookup"><span data-stu-id="05af2-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="05af2-113">OS</span><span class="sxs-lookup"><span data-stu-id="05af2-113">PARAMETERS</span></span>

### <span data-ttu-id="05af2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05af2-114">-DefaultProfile</span></span>
<span data-ttu-id="05af2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05af2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05af2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05af2-116">-InputObject</span></span>
<span data-ttu-id="05af2-117">Um objeto de conta de armazenamento, retornado por Get_AzStorageAccount, New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="05af2-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

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

### <span data-ttu-id="05af2-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05af2-118">-PassThru</span></span>
<span data-ttu-id="05af2-119">Normalmente, esse cmdlet não retorna nenhuma saída na conclusão bem-sucedida, esse parâmetro força o cmdlet a retornar um valor ($true) em uma conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="05af2-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="05af2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05af2-120">-ResourceGroupName</span></span>
<span data-ttu-id="05af2-121">O nome do grupo de recursos que contém o recurso da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="05af2-121">The resource group name containing the storage account resource.</span></span>

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

### <span data-ttu-id="05af2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05af2-122">-ResourceId</span></span>
<span data-ttu-id="05af2-123">ID do recurso da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="05af2-123">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="05af2-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="05af2-124">-StorageAccountName</span></span>
<span data-ttu-id="05af2-125">O nome do recurso da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="05af2-125">The name of the storage account resource.</span></span>

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

### <span data-ttu-id="05af2-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="05af2-126">-Confirm</span></span>
<span data-ttu-id="05af2-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05af2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05af2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05af2-128">-WhatIf</span></span>
<span data-ttu-id="05af2-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05af2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05af2-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05af2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05af2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05af2-131">CommonParameters</span></span>
<span data-ttu-id="05af2-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05af2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05af2-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05af2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05af2-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05af2-134">INPUTS</span></span>

### <span data-ttu-id="05af2-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05af2-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="05af2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="05af2-136">System.String</span></span>

## <span data-ttu-id="05af2-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05af2-137">OUTPUTS</span></span>

### <span data-ttu-id="05af2-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05af2-138">System.Boolean</span></span>

## <span data-ttu-id="05af2-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05af2-139">NOTES</span></span>

## <span data-ttu-id="05af2-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05af2-140">RELATED LINKS</span></span>
