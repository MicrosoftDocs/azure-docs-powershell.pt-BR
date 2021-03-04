---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
ms.openlocfilehash: b5d5da8c02081437f064fc1d2a6a29a5b772e8c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891831"
---
# <span data-ttu-id="f2154-101">Get-AzKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f2154-101">Get-AzKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="f2154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2154-102">SYNOPSIS</span></span>
<span data-ttu-id="f2154-103">Listar definições de função de um HSM gerenciado determinado em um determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="f2154-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="f2154-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f2154-104">SYNTAX</span></span>

### <span data-ttu-id="f2154-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f2154-105">Interactive (Default)</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2154-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f2154-106">ByName</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2154-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f2154-107">DESCRIPTION</span></span>
<span data-ttu-id="f2154-108">Listar definições de função de um HSM gerenciado determinado em um determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="f2154-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="f2154-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2154-109">EXAMPLES</span></span>

### <span data-ttu-id="f2154-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2154-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleDefinition -HsmName myHsm -Scope "/keys"

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="f2154-111">O exemplo lista todas as funções no escopo "/keys".</span><span class="sxs-lookup"><span data-stu-id="f2154-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="f2154-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f2154-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzKeyVaultRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

PS C:\> $backupRole.Permissions

AllowedActions DeniedActions AllowedDataActions DeniedDataActions
-------------- ------------- ------------------ -----------------
0 action(s)    0 action(s)   3 action(s)        0 action(s)

PS C:\> $backupRole.Permissions.AllowedDataActions

Microsoft.KeyVault/managedHsm/backup/start/action
Microsoft.KeyVault/managedHsm/backup/status/action
Microsoft.KeyVault/managedHsm/keys/backup/action

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="f2154-113">O exemplo obtém a função "Backup HSM Gerenciado" e inspeciona suas permissões.</span><span class="sxs-lookup"><span data-stu-id="f2154-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="f2154-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f2154-114">PARAMETERS</span></span>

### <span data-ttu-id="f2154-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2154-115">-DefaultProfile</span></span>
<span data-ttu-id="f2154-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2154-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2154-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="f2154-117">-HsmName</span></span>
<span data-ttu-id="f2154-118">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="f2154-118">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2154-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f2154-119">-RoleDefinitionName</span></span>
<span data-ttu-id="f2154-120">Nome da definição de função a ser obter.</span><span class="sxs-lookup"><span data-stu-id="f2154-120">Name of the role definition to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2154-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="f2154-121">-Scope</span></span>
<span data-ttu-id="f2154-122">Escopo no qual a atribuição ou definição de função se aplica, por exemplo, '/' ou '/keys' ou '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="f2154-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="f2154-123">'/' é usado quando omitido.</span><span class="sxs-lookup"><span data-stu-id="f2154-123">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2154-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2154-124">CommonParameters</span></span>
<span data-ttu-id="f2154-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2154-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2154-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2154-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2154-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2154-127">INPUTS</span></span>

### <span data-ttu-id="f2154-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f2154-128">None</span></span>

## <span data-ttu-id="f2154-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f2154-129">OUTPUTS</span></span>

### <span data-ttu-id="f2154-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f2154-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="f2154-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="f2154-131">NOTES</span></span>

## <span data-ttu-id="f2154-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2154-132">RELATED LINKS</span></span>
