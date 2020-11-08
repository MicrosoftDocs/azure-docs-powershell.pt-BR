---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
ms.openlocfilehash: 60ba6fbf57fa9e1ac9e25a913fb9755902b56ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115307"
---
# <span data-ttu-id="fc140-101">Get-AzManagedHsmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="fc140-101">Get-AzManagedHsmRoleDefinition</span></span>

## <span data-ttu-id="fc140-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc140-102">SYNOPSIS</span></span>
<span data-ttu-id="fc140-103">Listar definições de função de um determinado HSM gerenciado em um determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="fc140-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="fc140-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc140-104">SYNTAX</span></span>

### <span data-ttu-id="fc140-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="fc140-105">Interactive (Default)</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc140-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fc140-106">ByName</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc140-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc140-107">DESCRIPTION</span></span>
<span data-ttu-id="fc140-108">Listar definições de função de um determinado HSM gerenciado em um determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="fc140-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="fc140-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc140-109">EXAMPLES</span></span>

### <span data-ttu-id="fc140-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fc140-110">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleDefinition -HsmName myHsm -Scope "/keys"

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

<span data-ttu-id="fc140-111">O exemplo lista todas as funções no escopo "/Keys".</span><span class="sxs-lookup"><span data-stu-id="fc140-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="fc140-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fc140-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzManagedHsmRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

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

<span data-ttu-id="fc140-113">O exemplo obtém a função "backup do HSM gerenciado" e inspeciona suas permissões.</span><span class="sxs-lookup"><span data-stu-id="fc140-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="fc140-114">OS</span><span class="sxs-lookup"><span data-stu-id="fc140-114">PARAMETERS</span></span>

### <span data-ttu-id="fc140-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc140-115">-DefaultProfile</span></span>
<span data-ttu-id="fc140-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc140-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc140-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="fc140-117">-HsmName</span></span>
<span data-ttu-id="fc140-118">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="fc140-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="fc140-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="fc140-119">-RoleDefinitionName</span></span>
<span data-ttu-id="fc140-120">Nome da definição de função a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="fc140-120">Name of the role definition to get.</span></span>

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

### <span data-ttu-id="fc140-121">-Escopo</span><span class="sxs-lookup"><span data-stu-id="fc140-121">-Scope</span></span>
<span data-ttu-id="fc140-122">Escopo no qual a atribuição de função ou definição se aplica, por exemplo, '/' ou '/Keys ' ou '/keys/{keyName} '.</span><span class="sxs-lookup"><span data-stu-id="fc140-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="fc140-123">'/' é usado quando omitido.</span><span class="sxs-lookup"><span data-stu-id="fc140-123">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="fc140-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc140-124">CommonParameters</span></span>
<span data-ttu-id="fc140-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc140-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc140-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc140-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc140-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc140-127">INPUTS</span></span>

### <span data-ttu-id="fc140-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fc140-128">None</span></span>

## <span data-ttu-id="fc140-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc140-129">OUTPUTS</span></span>

### <span data-ttu-id="fc140-130">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="fc140-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="fc140-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc140-131">NOTES</span></span>

## <span data-ttu-id="fc140-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc140-132">RELATED LINKS</span></span>
