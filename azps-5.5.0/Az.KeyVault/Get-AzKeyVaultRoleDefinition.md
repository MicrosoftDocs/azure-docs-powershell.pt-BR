---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
ms.openlocfilehash: 6e4f58c355296a281a9ecbef21d7eca754bf41c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113758"
---
# <span data-ttu-id="30d03-101">Get-AzKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="30d03-101">Get-AzKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="30d03-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30d03-102">SYNOPSIS</span></span>
<span data-ttu-id="30d03-103">Definições de função de lista de um HSM gerenciado determinado em um determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="30d03-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="30d03-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30d03-104">SYNTAX</span></span>

### <span data-ttu-id="30d03-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="30d03-105">Interactive (Default)</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30d03-106">ByName</span><span class="sxs-lookup"><span data-stu-id="30d03-106">ByName</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30d03-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="30d03-107">DESCRIPTION</span></span>
<span data-ttu-id="30d03-108">Definições de função de lista de um HSM gerenciado determinado em um determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="30d03-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="30d03-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="30d03-109">EXAMPLES</span></span>

### <span data-ttu-id="30d03-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="30d03-110">Example 1</span></span>
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

<span data-ttu-id="30d03-111">O exemplo lista todas as funções no escopo "/chaves".</span><span class="sxs-lookup"><span data-stu-id="30d03-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="30d03-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="30d03-112">Example 2</span></span>
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

<span data-ttu-id="30d03-113">O exemplo obtém a função "Backup HSM Gerenciado" e inspeciona suas permissões.</span><span class="sxs-lookup"><span data-stu-id="30d03-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="30d03-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30d03-114">PARAMETERS</span></span>

### <span data-ttu-id="30d03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d03-115">-DefaultProfile</span></span>
<span data-ttu-id="30d03-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="30d03-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30d03-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="30d03-117">-HsmName</span></span>
<span data-ttu-id="30d03-118">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="30d03-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="30d03-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="30d03-119">-RoleDefinitionName</span></span>
<span data-ttu-id="30d03-120">Nome da definição de função a ser obter.</span><span class="sxs-lookup"><span data-stu-id="30d03-120">Name of the role definition to get.</span></span>

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

### <span data-ttu-id="30d03-121">-Escopo</span><span class="sxs-lookup"><span data-stu-id="30d03-121">-Scope</span></span>
<span data-ttu-id="30d03-122">Escopo no qual a atribuição ou definição da função se aplica, por exemplo, '/' ou '/keys' ou '/keys/{keyName}'.</span><span class="sxs-lookup"><span data-stu-id="30d03-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="30d03-123">'/' é usado quando omitido.</span><span class="sxs-lookup"><span data-stu-id="30d03-123">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="30d03-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d03-124">CommonParameters</span></span>
<span data-ttu-id="30d03-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30d03-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d03-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30d03-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d03-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="30d03-127">INPUTS</span></span>

### <span data-ttu-id="30d03-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="30d03-128">None</span></span>

## <span data-ttu-id="30d03-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="30d03-129">OUTPUTS</span></span>

### <span data-ttu-id="30d03-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="30d03-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="30d03-131">Notas</span><span class="sxs-lookup"><span data-stu-id="30d03-131">NOTES</span></span>

## <span data-ttu-id="30d03-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30d03-132">RELATED LINKS</span></span>
