---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/set-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b52dc34ddffb2234962888407ed67c487f4195c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112509"
---
# <span data-ttu-id="8f7c8-101">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8f7c8-101">Set-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="8f7c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f7c8-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7c8-103">Cria ou modifica a política de gerenciamento de uma conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-103">Creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="8f7c8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f7c8-104">SYNTAX</span></span>

### <span data-ttu-id="8f7c8-105">AccountNamePolicyRule (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8f7c8-105">AccountNamePolicyRule (Default)</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Rule <PSManagementPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f7c8-106">AccountNamePolicyObject</span><span class="sxs-lookup"><span data-stu-id="8f7c8-106">AccountNamePolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Policy <PSManagementPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f7c8-107">AccountObjectPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8f7c8-107">AccountObjectPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f7c8-108">AccountObjectPolicyObject</span><span class="sxs-lookup"><span data-stu-id="8f7c8-108">AccountObjectPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f7c8-109">AccountResourceIdPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8f7c8-109">AccountResourceIdPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f7c8-110">AccountResourceIdPolicyObject</span><span class="sxs-lookup"><span data-stu-id="8f7c8-110">AccountResourceIdPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f7c8-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f7c8-111">DESCRIPTION</span></span>
<span data-ttu-id="8f7c8-112">O cmdlet **Set-AzStorageAccountManagementPolicy** cria ou modifica a política de gerenciamento de uma conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-112">The **Set-AzStorageAccountManagementPolicy** cmdlet creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="8f7c8-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f7c8-113">EXAMPLES</span></span>

### <span data-ttu-id="8f7c8-114">Exemplo 1: Criar ou atualizar a política de gerenciamento de uma conta de armazenamento com objetos de regra ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-114">Example 1: Create or update the management policy of a Storage account with ManagementPolicy rule objects.</span></span>
```
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter1 = New-AzStorageAccountManagementPolicyFilter -PrefixMatch ab,cd 
PS C:\>$rule1 = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action1 -Filter $filter1

PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$filter2 = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule2 = New-AzStorageAccountManagementPolicyRule -Name Test2 -Action $action2 -Filter $filter2

PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule1,$rule2


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:29:29 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  30
                                                                                                },
                                                                                 "TierToArchive":  {
                                                                                                       "DaysAfterModificationGreaterThan":  50
                                                                                                   },
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  {
                                                                                 "Delete":  {
                                                                                                "DaysAfterCreationGreaterThan":  100
                                                                                            }
                                                                             }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  [
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="8f7c8-115">Primeiro, este comando cria 2 objetos de regra ManagementPolicy e, em seguida, cria ou atualiza a política de gerenciamento de uma conta de Armazenamento com os 2 objetos de regra ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-115">This command first create 2 ManagementPolicy rule objects, then creates or updates the management policy of a Storage account with the 2 ManagementPolicy rule objects.</span></span>

### <span data-ttu-id="8f7c8-116">Exemplo 2: Criar ou atualizar a política de gerenciamento de uma conta de armazenamento com uma política de formato Json.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-116">Example 2: Create or update the management policy of a Storage account with a Json format policy.</span></span>
```
PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Policy (@{
    Rules=(@{
        Enabled=$true;
        Name="Test";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=@{DaysAfterModificationGreaterThan=30};
                    TierToArchive=@{DaysAfterModificationGreaterThan=50};
                    Delete=@{DaysAfterModificationGreaterThan=100};
                });
                Snapshot=(@{
                    Delete=@{DaysAfterCreationGreaterThan=100};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
                PrefixMatch=@("prefix1","prefix2");
            })
        })
    },
    @{
        Enabled=$false;
        Name="Test2";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=@{DaysAfterModificationGreaterThan=80};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
            })
        })
    })
})


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:24:55 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  30
                                                                                                },
                                                                                 "TierToArchive":  {
                                                                                                       "DaysAfterModificationGreaterThan":  50
                                                                                                   },
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  {
                                                                                 "Delete":  {
                                                                                                "DaysAfterCreationGreaterThan":  100
                                                                                            }
                                                                             }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  [
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  false,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  80
                                                                                                },
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  null
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="8f7c8-117">Esse comando cria ou atualiza a política de gerenciamento de uma conta de Armazenamento com uma política de formato json.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-117">This command creates or updates the management policy of a Storage account with a json format policy.</span></span>

### <span data-ttu-id="8f7c8-118">Exemplo 3: Obter a política de gerenciamento de uma conta de Armazenamento e defini-la para outra conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-118">Example 3: Get the management policy from a Storage account, then set it to another Storage account.</span></span>
```
PS C:\>$outputPolicy = Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" | Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup2" -AccountName "mystorageaccount2"
```

<span data-ttu-id="8f7c8-119">Esse comando obtém primeiro a política de gerenciamento de uma conta de Armazenamento e, em seguida, a configura para outra conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-119">This command first gets the management policy from a Storage account, then set it to another Storage account.</span></span>

## <span data-ttu-id="8f7c8-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f7c8-120">PARAMETERS</span></span>

### <span data-ttu-id="8f7c8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7c8-121">-DefaultProfile</span></span>
<span data-ttu-id="8f7c8-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f7c8-123">-Política</span><span class="sxs-lookup"><span data-stu-id="8f7c8-123">-Policy</span></span>
<span data-ttu-id="8f7c8-124">Objeto de Política de Gerenciamento para Definir</span><span class="sxs-lookup"><span data-stu-id="8f7c8-124">Management Policy Object to Set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: AccountNamePolicyObject, AccountObjectPolicyObject, AccountResourceIdPolicyObject
Aliases: ManagementPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7c8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7c8-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f7c8-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7c8-127">-Regra</span><span class="sxs-lookup"><span data-stu-id="8f7c8-127">-Rule</span></span>
<span data-ttu-id="8f7c8-128">As regras de Política de Gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-128">The Management Policy rules.</span></span> <span data-ttu-id="8f7c8-129">Obter o objeto com New-AzStorageAccountManagementPolicyRule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-129">Get the object with New-AzStorageAccountManagementPolicyRule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule[]
Parameter Sets: AccountNamePolicyRule, AccountObjectPolicyRule, AccountResourceIdPolicyRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7c8-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8f7c8-130">-StorageAccount</span></span>
<span data-ttu-id="8f7c8-131">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8f7c8-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectPolicyRule, AccountObjectPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7c8-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8f7c8-132">-StorageAccountName</span></span>
<span data-ttu-id="8f7c8-133">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7c8-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8f7c8-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="8f7c8-135">ID do Recurso de Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-135">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceIdPolicyRule, AccountResourceIdPolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7c8-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8f7c8-136">-Confirm</span></span>
<span data-ttu-id="8f7c8-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7c8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7c8-138">-WhatIf</span></span>
<span data-ttu-id="8f7c8-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f7c8-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7c8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7c8-141">CommonParameters</span></span>
<span data-ttu-id="8f7c8-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7c8-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f7c8-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7c8-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="8f7c8-144">INPUTS</span></span>

### <span data-ttu-id="8f7c8-145">System.String</span><span class="sxs-lookup"><span data-stu-id="8f7c8-145">System.String</span></span>

## <span data-ttu-id="8f7c8-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="8f7c8-146">OUTPUTS</span></span>

### <span data-ttu-id="8f7c8-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8f7c8-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span></span>

## <span data-ttu-id="8f7c8-148">Notas</span><span class="sxs-lookup"><span data-stu-id="8f7c8-148">NOTES</span></span>

## <span data-ttu-id="8f7c8-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f7c8-149">RELATED LINKS</span></span>
