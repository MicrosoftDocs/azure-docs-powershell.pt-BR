---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113932"
---
# <span data-ttu-id="db67e-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="db67e-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="db67e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db67e-102">SYNOPSIS</span></span>
<span data-ttu-id="db67e-103">Revogar todas as chaves de Delegação de Usuários de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="db67e-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="db67e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db67e-104">SYNTAX</span></span>

### <span data-ttu-id="db67e-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db67e-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db67e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="db67e-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db67e-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="db67e-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db67e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="db67e-108">DESCRIPTION</span></span>
<span data-ttu-id="db67e-109">O **cmdlet Revoke-AzStorageAccountUserDelegationKeys** revoga todas as chaves de Delegação de Usuário de uma conta de Armazenamento, portanto, todos os tokens SAS de identidade da conta de armazenamento também serão revogados.</span><span class="sxs-lookup"><span data-stu-id="db67e-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="db67e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db67e-110">EXAMPLES</span></span>

### <span data-ttu-id="db67e-111">Exemplo 1: Revogar todas as chaves de Delegação de Usuários de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="db67e-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="db67e-112">Este exemplo revoga todas as chaves de Delegação de Usuários de uma conta de Armazenamento, para que todos os tokens SAS de identidade gerados a partir das teclas delegação de usuários também sejam revogados.</span><span class="sxs-lookup"><span data-stu-id="db67e-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="db67e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db67e-113">PARAMETERS</span></span>

### <span data-ttu-id="db67e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db67e-114">-DefaultProfile</span></span>
<span data-ttu-id="db67e-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db67e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db67e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db67e-116">-InputObject</span></span>
<span data-ttu-id="db67e-117">Um objeto de conta de armazenamento, retornado por Get_AzStorageAccount, New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="db67e-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

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

### <span data-ttu-id="db67e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db67e-118">-PassThru</span></span>
<span data-ttu-id="db67e-119">Normalmente, esse cmdlet não retorna saída após a conclusão bem-sucedida, esse parâmetro força o cmdlet a retornar um valor ($true) na conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="db67e-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="db67e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db67e-120">-ResourceGroupName</span></span>
<span data-ttu-id="db67e-121">O nome do grupo de recursos que contém o recurso de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="db67e-121">The resource group name containing the storage account resource.</span></span>

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

### <span data-ttu-id="db67e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db67e-122">-ResourceId</span></span>
<span data-ttu-id="db67e-123">ID do Recurso de Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="db67e-123">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="db67e-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="db67e-124">-StorageAccountName</span></span>
<span data-ttu-id="db67e-125">O nome do recurso de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="db67e-125">The name of the storage account resource.</span></span>

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

### <span data-ttu-id="db67e-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="db67e-126">-Confirm</span></span>
<span data-ttu-id="db67e-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db67e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db67e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db67e-128">-WhatIf</span></span>
<span data-ttu-id="db67e-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="db67e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db67e-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db67e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db67e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db67e-131">CommonParameters</span></span>
<span data-ttu-id="db67e-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db67e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db67e-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db67e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db67e-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="db67e-134">INPUTS</span></span>

### <span data-ttu-id="db67e-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db67e-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="db67e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="db67e-136">System.String</span></span>

## <span data-ttu-id="db67e-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="db67e-137">OUTPUTS</span></span>

### <span data-ttu-id="db67e-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db67e-138">System.Boolean</span></span>

## <span data-ttu-id="db67e-139">Notas</span><span class="sxs-lookup"><span data-stu-id="db67e-139">NOTES</span></span>

## <span data-ttu-id="db67e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db67e-140">RELATED LINKS</span></span>
